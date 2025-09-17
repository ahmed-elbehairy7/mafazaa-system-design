---
trigger: always_on
---

# Drawing Instructions and Patterns

## Overview

This document provides guidance for creating and modifying diagrams in this repository. Always refer to existing drawings as reference to maintain consistency.

## General Guidelines

1. Use established color schemes:

    - Light blue (#dae8fc) for API endpoints and flows
    - Light yellow (#fff2cc) for validation/decision steps
    - Light red (#f8cecc) for error states and alerts
    - Light green (#d5e8d4) for success states
    - Gray background (#ffffff) for general sections
    - Orange (#ED7100) for compute resources
    - Purple (#C925D1) for database services
    - Red (#DD344C) for IAM roles and permissions
    - Blue (#8C4FFF) for networking components

2. Follow AWS diagram conventions:

    - Use official AWS icon set
    - Group resources by region and AZ
    - Layer VPC, subnet, and security group containers
    - Color code by service type
    - Include monitoring and alarm components

3. Maintain consistent layout patterns:
    - Top-down flow for process diagrams
    - Left-to-right for website/user flows
    - Nested containers for infrastructure
    - Group related components with clear boundaries

## Diagram-Specific Patterns

### Website Flow Diagrams

-   Use rounded rectangles for user interface states
-   Connect pages with directional arrows
-   Include Arabic titles for user-facing elements
-   Group related pages/functionalities vertically
-   Add explanatory notes for each component
-   Show validation steps and error states
-   Include user action flows and transitions
-   Represent modals and popups distinctly
-   Document success/completion states

### Process Flow Diagrams

-   Start with clear input/trigger state
-   Use diamonds for decision points
-   Include all validation and branching logic
-   Show error handling paths
-   Document success and failure states
-   Add caching/optimization steps
-   Include database interactions
-   Show external service calls
-   Document retry/fallback logic

### AWS Infrastructure Diagrams

-   Follow official AWS architectural patterns
-   Create clear VPC boundaries
-   Document all security groups
-   Show instance types and counts
-   Include all IAM roles and policies
-   Document IP ranges and subnets
-   Show load balancer configurations
-   Include monitoring and logging
-   Add scaling components and rules
-   Document backup and failover
-   Show cross-AZ redundancy
-   Include CloudWatch alarms

### Requirements Documentation

-   Split into functional/non-functional sections
-   Include scalability requirements
-   Document availability needs
-   Specify latency requirements
-   List consistency requirements
-   Document capacity planning
-   Include security requirements
-   Specify monitoring needs
-   List backup/recovery requirements

## Visual Elements

1. Decision Points:

    - Use rhombus shapes
    - Show clear yes/no paths
    - Include validation criteria
    - Document error conditions
    - Show caching checks
    - Include permission validation

2. State Boxes:

    - Rounded corners for UI states
    - Sharp corners for system processes
    - Consistent sizing per type
    - Clear entry/exit points
    - Include status indicators

3. Connections:

    - Orthogonal routing for flow lines
    - Clear directional arrows
    - Label all transitions
    - Show async vs sync flows
    - Document retry logic
    - Include fallback paths

4. Grouping:
    - Clear container boundaries
    - Consistent padding
    - Logical component grouping
    - Show service boundaries
    - Include environment separation

## Data Flow Elements

1. Cache Layers:

    - Show Redis instances
    - Document TTL policies
    - Include refresh logic
    - Show cache hierarchies

2. Database Interactions:

    - Show read/write patterns
    - Document consistency levels
    - Include replication flows
    - Show backup processes

3. API Flows:

    - Document endpoints
    - Show request/response
    - Include validation
    - Show rate limiting
    - Document authentication

4. Security:
    - Show IAM roles
    - Include security groups
    - Document access patterns
    - Show encryption points

## Review Process

Before committing new diagrams:

1. Compare with existing examples
2. Check color scheme consistency
3. Verify component alignment
4. Ensure proper labeling
5. Add explanatory notes
6. Validate security patterns
7. Check scaling components
8. Verify monitoring inclusion

Reference existing diagrams for:

-   Color schemes and visual patterns
-   Layout and flow organization
-   Component naming conventions
-   Service grouping patterns
-   Infrastructure patterns
-   Security implementations
-   Monitoring configurations
-   Scaling approaches
