# 🛍️ E-commerce Performance Testing using Apache JMeter

## 📖 Project Overview
This project tests the performance of the demo e-commerce site [Practice Automation Testing](https://practice.automationtesting.in) using **Apache JMeter**.  
It simulates multiple users visiting the homepage, adding items to the cart, and performing checkout to measure load time, error rate, and throughput.

---

## ⚙️ Tools & Technologies
- **Apache JMeter 5.6+**
- **Java JDK 8 or above**
- **Windows / macOS / Linux**
- **Browser (for manual reference)**
- **GitHub** (for version control)

---

## 🧩 Test Scenarios
| Test ID | Scenario | Request Type | Description |
|----------|-----------|---------------|--------------|
| T1 | Homepage Load | GET | Load main page to check response time |
| T2 | Add to Cart | POST | Simulate adding product to shopping cart |
| T3 | Checkout | GET | Simulate visiting checkout page |
| T4 | View Report | - | Collect metrics like response time, error %, and throughput |

---

## 🚀 How to Run
1. **Open JMeter**
2. Load the test plan:  
   `File → Open → Ecommerce_Performance_Test.jmx`
3. Configure **Thread Group**:
   - Users: `10`
   - Ramp-up: `5s`
   - Loop Count: `2`
4. Run the test ▶️
5. View results in:
   - **Summary Report**
   - **Aggregate Report**
   - **Graph Results**
6. Save results:  
   Export `.jtl` and generate HTML report:


📈 Sample Results
| Test        | Users | Avg Response (ms) | Error % | Throughput (req/sec) |
| ----------- | ----- | ----------------- | ------- | -------------------- |
| Homepage    | 10    | 1200              | 0       | 4.5                  |
| Add to Cart | 10    | 1350              | 0       | 4.3                  |
| Checkout    | 10    | 1800              | 1       | 3.9                  |


   ```bash
   jmeter -g results/results.jtl -o results/report
