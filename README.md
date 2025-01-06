BloodBridge: Optimizing Lifesaving Blood Resources
🚑 BloodBridge is a system designed to streamline emergency blood donation processes by matching blood requests with donors and notifying them about their nearest blood banks. This project integrates Flask, Twilio, and data-driven decision-making to create a scalable and impactful solution.

Features
Match Requests with Donors: Identify donors based on blood type.
Automated Notifications: Send SMS alerts to donors about emergency needs.
Nearest Blood Bank Details: Include the location of the nearest blood bank for donors.
Track Last Donation Dates: Filter donors based on eligibility (e.g., donation intervals).
Tech Stack
Backend: Python, Flask
SMS Notifications: Twilio API
Database: CSV (Demo), AWS-hosted database (Future)
Hosting: Local environment (Demo), AWS Cloud (Future)
Demo Setup
Prerequisites
Python 3.7 or above
Install required libraries:
bash
Copy code
pip install flask pandas twilio
A valid Twilio account for SMS notifications.
Installation
Clone the repository:

bash
Copy code

Project Status:
This is the initial stage of the project. I will be updating it into a fully functional website intended for a blood donation organization. The project will include features for managing blood donations, donor registration, and connecting with blood banks. Further updates will include website development, cloud deployment, and additional functionalities to enhance user experience.

git clone <repo-url>
cd BloodBridge
Place your donors.csv file in the root directory. Ensure it has the following columns:

text
Copy code
donor_id, name, blood_type, location, email, last_donated, phone_number
Update Twilio credentials in the Python script:

python
Copy code
twilio_sid = "your_twilio_account_sid"
twilio_auth_token = "your_twilio_auth_token"
twilio_phone_number = "your_twilio_phone_number"
Start the Flask server:

bash
Copy code
python app.py
Open Postman to test the APIs or use curl.

Testing the Demo
Endpoint 1: POST /request_blood
Send a JSON request to match donors based on blood type and notify them:

URL: http://127.0.0.1:5000/request_blood
Method: POST
Body (JSON):
json
Copy code
{
  "blood_type": "O+"
}
Response:

200: List of matched donors and SMS notifications sent.
404: No matching donors found.
Future Developments
Website Integration: Develop a web interface for users to submit requests and manage donations.
Cloud Hosting: Host the website and database on AWS for better scalability.
Advanced Features:
Filter donors based on last donation date.
Include proximity-based recommendations for blood banks.
Contributing
Fork the repository.
Create a new branch (git checkout -b feature/YourFeature).
Commit your changes (git commit -m "Add your feature").
Push to the branch (git push origin feature/YourFeature).
Open a Pull Request.
License
This project is licensed under the MIT License.
