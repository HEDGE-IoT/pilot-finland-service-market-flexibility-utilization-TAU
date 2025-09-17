# SUC-FI-02.06 – Market-Based Flexibility Utilization

## General Information and Purpose

**Service Name/Title:** Market-Based Flexibility Utilization  
**Description and Purpose:** Participates in a market (e.g., local flexibility market) to procure flexibility as a predictive measure to manage congestion.  
**Owner/Contact Information:** TAU  

---

## Functional Requirements

- Use congestion planning data.  
- Translate flexibility needs into flexibility requests in the market.  
- Validate incoming data.  
- Harmonise the input data.  
- Receive necessary data from the message broker.  
- Send flexibility requests and related data to the data space connector.  
- Establish and maintain a secure connection to the data space connector.  

---

## Non-Functional Requirements

- Congestion planning data should be available for processing.  
- Incoming data must be valid.  
- **99.9% uptime** for the service.  
- Connection to the data space connector should always be available.  

---

## Service Interfaces

- **Visualization:** Grafana (or equivalent) will be used to visualize flexibility requests, procurement status, and related forecasts.  
- **API Integration:** Grafana uses a premade HTTP API; no additional service interfaces are required.  

---

## Data Model

- **Entities and Relationships:**  
  - Congestion forecasts  
  - Flexibility needs  
  - Market flexibility requests  
  - Market responses  
- **Database Schema:** To be aligned with congestion planning outputs and flexibility market standards.  

---

## Integration and Dependencies

- **External Dependencies:** Congestion management planning service.  
- **System Dependencies:** Grid congestion forecasts, DER data.  
- **Third-party Integrations:** Data space connector, Grafana visualization.  
- **HEDGE-IoT Integration:** Exchange flexibility signals with DERs through cloud-edge connections.  
- **Integration with App Store:** To be defined.  
- **Integration with Data Space:** Required for flexibility market operations.  

---

## Security and Privacy

- **Data Sensitivity:** Flexibility requests and grid data are critical infrastructure information.  
- **Access Control:** Role-based authentication for submitting and monitoring flexibility requests.  
- **Audit Logs:** All requests, responses, and transactions are logged for transparency and compliance.  

---

## Performance Considerations

- **Stress Testing:** Must handle a large number of simultaneous flexibility requests.  
- **Response Times:** Requests must be generated and submitted in time to participate in market operations.  

---

## Deployment and Environment

- **Configuration:** Service configured to connect securely with both message broker and data space connector.  
- **CI/CD:** Automated testing and deployment pipeline.  
- **Monitoring and Logging:** Continuous monitoring of uptime, request latency, and market outcomes.  

---

## Testing and Validation

- **Test Cases:** Validation of data harmonisation, market request generation, and congestion mitigation workflows.  
- **Automated Testing Tools:** Used for functional and non-functional testing.  
- **Acceptance Tests:** Ensure successful end-to-end integration with congestion management and market interfaces.  

