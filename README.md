a. Start the Flask service.
Run the Python Flask app:

python app.py
Make sure the Flask service is running on the expected address, say http://localhost:5000, and it is ready to make predictions.

a. Start the Spring Boot Service
Run the Spring Boot application:


mvn spring-boot:run
Make sure the Spring Boot service is running at the right address, like http://localhost:8080.

Open up Postman.
If you don't have Postman installed, get it here.
Open Postman and create a new collection to organize your API requests.
3. Get a Device
Endpoint: POST http://localhost:8080/api/devices
Headers:
Content-Type: application/json
Hey, just use the raw JSON data to add a new device. Like this:

{
"battery_power": 1200,
"blue": yeah,
"clock_speed": 2.0,
"dual_sim": true
"fc": 5,
"four_g": yeah,
"int_memory": 16,
"m_dep": 0.8,
"mobile_wt": 150,
"n_cores": 4,
"pc": 13,
"px_height": 800,
"px_width": 1200,
"ram": 2GB,
"sc_h": 10,
"sc_w": 5,
"talk_time": 20,
"three_g": true,
"touch_screen": yeah
"wifi": yeah
).
Expected Response: The response should include a unique device ID:

{
"ID": 1,
"battery_power": 1200,
.
}
4. Predict the Device Price
Endpoint: Get http://localhost:8080/api/devices/predict/{id}Headers None needed. So, the response should include the approximate price range.
