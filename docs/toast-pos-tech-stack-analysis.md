# Toast POS - Tech Stack Analysis

## Overview
Toast is a cloud-based Point of Sale (POS) system designed specifically for restaurants. The platform combines native mobile applications with cloud-based services to provide a comprehensive restaurant management solution.

## Programming Languages

### Backend
Toast operates as a **polyglot shop** with multiple programming languages used across different services:
- **PHP** - Predominantly used (Drupal framework)
- **Ruby** - Major backend language
- **Go** - Used for specific services
- **Java** - Used for specific services

### Frontend/Mobile
- **Native Android** - The Toast POS app is built using native Android APIs

## Tech Stack Components

### Mobile Application
- **Platform**: Native Android tablet-based application
- **Framework**: Built using native Android APIs
- **Libraries**: Open source libraries including Dagger (dependency injection)

### Backend Infrastructure
- **Messaging**: RabbitMQ (key messaging component)
- **Web Framework**: Drupal (PHP-based)
- **Cloud Services**: Multiple independent service environments

### Web Technologies
- **ASP.NET**
- **JavaScript**
- **jQuery**
- **Bugsnag** (error tracking)
- **Cloudflare** (CDN and security)

Total of 19+ technologies in the stack.

## Architecture Model

### Deployment Strategy: **Hybrid Cloud-Native with Multi-Device Support**

#### Device Architecture
- **Primary Device**: Native Android app for tablets (single codebase for Android devices)
- **Web Interface**: Toast Web - Configuration and reporting website accessible via browsers
- **Not cross-platform**: Built specifically for Android, not using frameworks like React Native or Flutter

#### Service Architecture
- **Cloud-Based Platform**: All core services run in the cloud
- **Microservices**: Multiple independent backend services using different languages based on team expertise and problem domain
- **REST APIs**: Provides RESTful API for integration with third-party services
  - Inbound APIs: Partners call Toast services
  - Outbound APIs: Toast platform calls partner API servers
- **Service Environments**: Maintains separate sandbox and production environments

### Data Flow
1. **Native Android App** → Communicates with cloud services
2. **Cloud Services** → Handle business logic, data processing, and integrations
3. **REST APIs** → Enable third-party integrations and data exchange
4. **Toast Web** → Web-based configuration and reporting interface

## Integration Capabilities

### API Features
- RESTful web service APIs for location data management
- Sandbox environment for development and testing
- Partner integration program with formal application process
- Support for custom API development
- Bidirectional API communication (inbound and outbound)

### Developer Resources
- API reference documentation
- Downloadable APK installer for sandbox environment
- Multiple service environments for development, testing, and production
- Integration partner program

## Key Characteristics

### Advantages of This Architecture
1. **Native Performance**: Android-native app provides optimal performance and device integration
2. **Flexibility**: Polyglot backend allows teams to choose the best language for each service
3. **Scalability**: Cloud-based infrastructure enables horizontal scaling
4. **Integration-Friendly**: Comprehensive REST API enables extensive third-party integrations

### Platform Strategy
- **Single Native Platform**: Focused on Android tablets rather than supporting multiple mobile OS platforms
- **Cloud-First**: All business logic and data processing handled in the cloud
- **API-Driven**: Strong emphasis on integrations and partner ecosystem
- **Restaurant-Specific**: Purpose-built for restaurant operations

## Summary

Toast POS uses a **native Android application** connected to a **polyglot cloud-based backend** architecture. It is NOT a single service for all devices - instead, it's a native Android app that communicates with multiple cloud-based microservices. The backend services are written in multiple languages (PHP, Ruby, Go, Java) and communicate through RabbitMQ messaging. The platform provides both a mobile POS application and a web-based configuration interface, all connected through cloud services and REST APIs.

---

## Sources
- [Toast Tech Stack - Himalayas.app](https://himalayas.app/companies/toast/tech-stack)
- [Toast POS Integrations and APIs](https://pos.toasttab.com/integrations)
- [Toast Inc. Technology Stack](https://rocketreach.co/toast-inc-technology-stack_b4576a39fca59be8)
- [Toast - Tech Stack, Apps, Patents & Trademarks](https://www.crunchbase.com/organization/toast/technology)
- [Toast platform overview](https://doc.toasttab.com/doc/platformguide/platformToastPlatformOverview.html)
- [Behind the scenes: How Boston tech companies chose their tech stacks](https://www.builtinboston.com/articles/behind-scenes-how-boston-tech-companies-chose-technology-stack)
- [Developer guide](https://doc.toasttab.com/doc/devguide/index.html)
- [What are the technologies used by Toast?](https://stackshare.io/companies/toast)
- [Sandbox environment](https://doc.toasttab.com/doc/devguide/apiEnvironments.html)
- [API overview](https://doc.toasttab.com/doc/devguide/apiOverview.html)
