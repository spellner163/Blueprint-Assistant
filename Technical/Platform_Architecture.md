# Platform Architecture

## 3-Tier Distributed Architecture
Blueprint uses minimum 3-server distributed architecture (not monolithic or microservices):

### Web Server Layer
- **Dual IIS Application Pools:** Public Blueprint (internet) + Auxiliary Services (internal)
- **Handles:** Synchronous operations (search, file download/upload, login)

### Database Server Layer
- **Technology:** SQL Server cluster
- **Function:** Data storage and retrieval

### Job Server Layer
- **Purpose:** Asynchronous work processing (30 seconds to 30 minutes)
- **Contains:** Import/export, document generation, image rendering, diagram creation
- **Customer Isolation:** Dedicated pools, sites, job services, database connections per customer

## Common Object Model (COM)

### Architecture
- **Hub-and-spoke** translation layer
- Converts all RPA formats (UiPath, Blue Prism, A360) to Blueprint proprietary language
- Single export target: Power Automate Desktop

### Data Structure
- **Dual-layer:**
  - Raw parameters tab: Complete action and code from source tool
  - Parsed parameter-level information for each action
- **Philosophy:** Prefer blank parameters over missing critical data

### Scalability
- Adding new RPA tool requires only one new parser
- Microsoft API updates benefit all source tools simultaneously
- Single source of truth for all migrations

## Migration Process Flow
1. **Web server** receives RPA file → queues job
2. **Job server import** validates/parses → stores raw data in database
3. **Job server processing** converts to COM → stores COM data
4. **Job server export** converts COM to PAD → sends to Microsoft APIs/exports file
5. **Web server** displays results from database

## Infrastructure Strategy

### Production - Rackspace
- **Configuration:** Dedicated servers, full racks, firewalls, load balancers
- **Positioning:** "Private cloud" for enterprise sales
- **Benefits:** Windows patching automation, granular scaling (add 2 cores individually), avoids AWS cost doubling at thresholds

### Development - AWS
- **Use:** Public cloud for dev work
- **Advantages:** Cheap, can scale 3 dev sites in 10 minutes
- **Sites:** Dev 1-4, QA, Perf stack for pre-release builds
- **Risk Management:** Memory leaks in untested builds won't impact production

### Deployment
- **Production rule:** Customer/partner sites always Rackspace
- **Dev rule:** Pre-release builds on AWS for risk isolation
- **Tools:** AWS uses Jenkins, Rackspace uses Ansible (faster for updates near RTM)

## Testing Strategy
- **Nightly CI/CD:** Benchmark processes from all supported RPA tools
- **Target Metric:** 75% migration success rate (low-80s actual: 90% simple, 60-70% complex)
- **On-Premise Testing:** Risk analysis on new Windows Server/SQL versions, tested ~twice yearly
