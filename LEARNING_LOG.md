# AWS Cloud Portfolio - Development Log

> **Real-time tracking of my AWS cloud infrastructure project - from complete beginner to working full-stack application**

## Project Status Overview

**Current Phase:** Phase 2 Complete - EC2 API Server Deployed ✅  
**Started:** 09-06-2025  
**Latest Update:** 15-06-2025  
**Overall Progress:** 50% Complete - Frontend and Backend Running  

**Live Infrastructure:**
- **S3 Website:** (http://pranav-portfolio-2024.s3-website-us-east-1.amazonaws.com)
- **EC2 API Server:** http://44.202.148.167:3000/api/health

---

## 09-06-2025 - Day 1: Project Foundation & S3 Static Website

**What I accomplished today:**
- Set up GitHub repository structure for professional documentation
- Created HTML/CSS website files (index.html, styles.css)
- Learned about Amazon S3 and static website hosting capabilities
- Successfully created AWS account and navigated the console for the first time

**Technical implementation:**
- Designed responsive website with modern CSS Grid and Flexbox
- Implemented mobile-first design approach
- Created professional color scheme and typography
- Structured content to showcase AWS learning progression

**S3 Configuration Process:**
- Created S3 bucket with globally unique name
- Configured static website hosting with index.html as entry point
- Set up bucket policy for public read access (learned JSON policy syntax)
- Uploaded website files and verified accessibility

**The 404 debugging experience:**
- Initially got "NoSuchKey: index.html" error
- Discovered file upload location matters (root vs subfolders)
- Learned difference between S3 object URLs and website endpoints
- Successfully resolved by ensuring files were in bucket root

**Key learning moments:**
- AWS Console navigation is intimidating at first but logical once you understand the structure
- Bucket names must be globally unique across ALL AWS accounts (not just yours)
- S3 static hosting is incredibly fast and reliable
- Public access configuration requires careful balance of security and functionality

**Challenges overcome:**
- Understanding S3 bucket policies (JSON syntax was new to me)
- Configuring public access without compromising security
- File organization and upload location troubleshooting

**Time invested:** 4 hours total
- 1 hour: GitHub setup and documentation
- 2 hours: HTML/CSS development 
- 1 hour: S3 configuration and troubleshooting

**Confidence level:** Excited and surprised by how quickly S3 website worked once configured properly

---

## Day 2: 🚀 PHASE 2 COMPLETE: EC2 Backend Server Deployed

**Major milestone achieved:**
Successfully deployed a Node.js API server on Amazon EC2 that's accessible from anywhere on the internet!

**What I built:**
- EC2 t2.micro instance running Amazon Linux
- Node.js 18.20.8 runtime environment
- Express.js API server with CORS enabled
- Three functional API endpoints:
  - `/api/health` - Server status and uptime monitoring
  - `/api/info` - Server information and environment details
  - `/api/contact` - Contact form submission handler

**Technical journey - EC2 setup:**
- Launched first EC2 instance using AWS Console
- Learned about instance types (t2.micro for free tier)
- Created and downloaded SSH key pair for secure access
- Used browser-based terminal instead of local SSH (easier for learning)

**Linux server administration learned:**
- Basic command navigation: `pwd`, `ls`, `cd`, `mkdir`
- File operations: `cat`, `nano` for editing
- Process management: `ps aux` to check running processes
- Package management: `yum update`, `yum install`
- Understanding user permissions and `sudo`

**Node.js development process:**
- Installed Node.js 18.x using official repository setup
- Created project structure with `npm init -y`
- Learned about package.json and dependency management
- Installed Express.js and CORS middleware
- Wrote server code from scratch using JavaScript

**AWS Security Groups configuration:**
- Understood AWS firewall concept (Security Groups)
- Added custom TCP rule for port 3000
- Learned about inbound vs outbound rules
- Configured public access for API endpoints while maintaining SSH security

**Debugging and troubleshooting experience:**
- Server initially wouldn't start due to missing package.json
- Learned to diagnose issues using `ps aux | grep node`
- Used `curl localhost:3000` for local testing before internet access
- Rebuilt project directory when files went missing
- Systematic approach: local testing first, then internet accessibility

**API endpoints working:**
- Health check returns JSON with server status, timestamp, and uptime
- Server info endpoint provides technical environment details
- Contact form handler ready for frontend integration
- All endpoints tested and responding correctly from the internet

**Screenshots of work done**
- Working website
  ![Website](https://github.com/user-attachments/assets/eedfab74-d398-45ea-8352-646d1a9cb212)
- EC2 terminal API
  ![EC2_Terminal API health](https://github.com/user-attachments/assets/b2454585-b01c-4ffa-a980-2ff46b75ff97)
- Website API URL test
  ![Website URL](https://github.com/user-attachments/assets/7eb68e72-ea08-4b84-b558-05271d1b109c)

**Key concepts mastered:**
- **Virtual servers in the cloud:** EC2 instances are like renting computers in Amazon's data centers
- **SSH and remote access:** Secure shell connections for server management
- **Linux basics:** Command line navigation and file system understanding
- **API development:** RESTful endpoints that respond to HTTP requests
- **Network security:** Firewall rules and port management
- **Process management:** Running services and keeping them alive

**Real-world skills gained:**
- Cloud server deployment and management
- Backend API development with Node.js
- Network security configuration
- Linux system administration basics
- Troubleshooting server connectivity issues

**Mistakes made and lessons learned:**
- Initially tried HTTPS instead of HTTP (SSL certificates needed for HTTPS)
- Forgot that browser-based terminals use right-click for pasting
- Had to recreate project files when npm commands didn't work properly
- Learned importance of verifying each step before moving to next

**Current architecture:**
```
Internet Users → S3 Static Website (Frontend)
Internet Users → EC2 API Server (Backend) ← LIVE AND WORKING!
```

**Time invested today:** 6 hours
- 2 hours: EC2 setup and initial connection
- 2 hours: Linux learning and Node.js installation
- 1.5 hours: Server code development and deployment
- 0.5 hours: Security group configuration and testing

**Technical validation:**
- API accessible at: http://44.202.148.167:3000/api/health
- Server responds with proper JSON formatting
- CORS configured for cross-origin requests
- Express.js middleware working correctly

---

## Cumulative Learning: What I Now Understand

### AWS Cloud Concepts
- **Infrastructure as a Service (IaaS):** EC2 provides virtual computers you manage
- **Platform as a Service (PaaS):** S3 provides web hosting without server management
- **Free Tier Strategy:** How to build real applications within AWS free limits
- **Regional Services:** Understanding where your resources are physically located

### Full-Stack Architecture
- **Frontend (S3):** Static files served globally with high availability
- **Backend (EC2):** Dynamic processing and API endpoints for data handling
- **Separation of Concerns:** UI logic vs business logic vs data storage
- **HTTP Communication:** How frontend and backend communicate via APIs

### Cloud Security Model
- **Network Security:** Security Groups as cloud firewalls
- **Access Control:** SSH keys vs passwords for server access
- **Public vs Private:** When to expose services to internet vs keep internal
- **Least Privilege:** Only opening required ports and permissions

### Development Operations (DevOps)
- **Server Provisioning:** Launching and configuring cloud infrastructure
- **Deployment Process:** Getting code from development to production
- **Monitoring and Testing:** Verifying services are working correctly
- **Troubleshooting:** Systematic approach to diagnosing and fixing issues

### Technical Skills Acquired
- **Linux Command Line:** Comfortable with basic server administration
- **Node.js Development:** Building APIs with Express.js framework
- **JSON Configuration:** Understanding AWS policies and package management
- **Network Debugging:** Using curl and browser tools to test connectivity
- **Version Control:** Organizing and documenting project progression

---

## Resources That Actually Helped

**AWS Documentation:** 
- S3 static website hosting guide was comprehensive
- EC2 getting started tutorial covered the basics well
- Security Groups documentation helped understand firewall concepts

**Command Line Learning:**
- Trial and error was the most educational approach
- AWS browser terminal made Linux accessible without local setup
- Stack Overflow for specific error messages and solutions

**Development Resources:**
- Node.js official documentation for installation procedures
- Express.js quick start guide for API development
- Mozilla Developer Network (MDN) for HTTP and web concepts

**Problem-Solving Approach:**
- Start with simplest possible implementation
- Test locally before testing remotely
- Use systematic debugging (check one thing at a time)
- Document what works and what doesn't

---

## Current Project Status

### Completed Infrastructure
- [x] **Amazon S3:** Static website hosting with global CDN capability
- [x] **Amazon EC2:** Virtual server running Node.js API backend
- [x] **Security Groups:** Network firewall configured for web traffic
- [x] **DNS Resolution:** Public IP addresses accessible from internet

### Working Features
- [x] Professional responsive website hosted on S3
- [x] RESTful API server with multiple endpoints
- [x] JSON data exchange between services
- [x] Cross-origin resource sharing (CORS) configured
- [x] Server health monitoring and status reporting

### Next Phase Opportunities
- [ ] **Frontend-Backend Integration:** Connect S3 website to EC2 API
- [ ] **Database Layer:** Add RDS for persistent data storage
- [ ] **SSL/HTTPS:** Implement encryption for secure communications
- [ ] **Domain Name:** Custom domain instead of AWS-generated URLs
- [ ] **Monitoring:** CloudWatch for performance and error tracking

---

## Technical Metrics and Performance

### Infrastructure Costs
- **Current Monthly Cost:** $0.00 (within free tier limits)
- **S3 Usage:** < 1GB storage, minimal requests
- **EC2 Usage:** 1 t2.micro instance, well within 750 hour/month limit
- **Data Transfer:** Minimal bandwidth usage for testing

### Performance Characteristics
- **S3 Website Load Time:** < 500ms globally
- **API Response Time:** ~50ms average for health checks
- **Server Uptime:** 100% since deployment
- **Error Rate:** 0% (all endpoints responding correctly)

### Scalability Considerations
- **Current Capacity:** Single EC2 instance suitable for learning/demo
- **Bottlenecks:** API server is single point of failure
- **Growth Path:** Load balancers, auto-scaling, multi-AZ deployment
- **Database Needs:** File-based storage not suitable for production

---

## Reflection: From Complete Beginner to Cloud Developer

**Starting Point:** Never used Linux, never deployed a server, basic web development knowledge

**Current State:** 
- Comfortable with AWS console navigation and service configuration
- Can deploy and manage cloud infrastructure using industry-standard practices
- Understanding of full-stack architecture and API development
- Troubleshooting skills for cloud connectivity and server issues

**Confidence Level:** Cautiously optimistic and genuinely excited about cloud capabilities

**Most Surprising Discovery:** How quickly you can go from idea to live, internet-accessible application using cloud services

**Biggest Challenge Overcome:** Learning Linux command line while simultaneously learning AWS concepts

**Skills Most Proud Of:** 
- Systematic troubleshooting approach when things don't work
- Ability to read documentation and translate it into working configurations
- Building something real that demonstrates practical cloud knowledge

**Ready for Next Challenge:** Eager to connect frontend and backend for complete full-stack experience

---

**Last Updated:** 15-06-2025  
**Next Session Goal:** Connect S3 frontend to EC2 backend with working contact form  
**Long-term Objective:** Complete 5-phase AWS portfolio demonstrating production-ready cloud architecture
