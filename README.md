# DivyaReddy9876weatherMonitor
Developed a real-time weather monitoring system using data from the OpenWeatherMap API. This project retrieves weather data for various metros in India at regular intervals, converts temperature values from Kelvin to Celsius, and calculates daily weather summaries including average, maximum, and minimum temperatures, as well as dominant weather conditions. The system also defines user-configurable alert thresholds for specific weather conditions and implements visualizations to display daily summaries and alerts. Data is stored in a database for further analysis. Key features include error handling for invalid data formats and support for additional weather parameters like humidity and wind speed.

Features:
Daily Summary:

Aggregate daily temps (avg, max, min) & dominant weather condition.
Store for analysis.
Alerts:

Set custom thresholds (e.g., temp > 35°C).
Trigger alerts when thresholds are exceeded.
Visualizations:

Show daily summaries, trends, and alerts.

Tests:
Setup: Check API connection.
Data: Simulate API calls.
Conversion: Validate temp conversions.
Summary: Verify daily summaries.
Alerts: Test alert triggers.


My python script output looks as follows:

{'coord': {'lon': 77.2167, 'lat': 28.6667}, 'weather': [{'id': 721, 'main': 'Haze', 'description': 'haze', 'icon': '50n'}], 'base': 'stations', 'main': {'temp': 299.2, 'feels_like': 299.2, 'temp_min': 299.2, 'temp_max': 299.2, 'pressure': 1011, 'humidity': 57, 'sea_level': 1011, 'grnd_level': 986}, 'visibility': 2500, 'wind': {'speed': 2.57, 'deg': 280}, 'clouds': {'all': 0}, 'dt': 1729709274, 'sys': {'type': 1, 'id': 9165, 'country': 'IN', 'sunrise': 1729731454, 'sunset': 1729771966}, 'timezone': 19800, 'id': 1273294, 'name': 'Delhi', 'cod': 200}
C:\Users\DELL\weatherMonitor.py:23: DeprecationWarning: datetime.datetime.utcfromtimestamp() is deprecated and scheduled for removal in a future version. Use timezone-aware objects to represent datetimes in UTC: datetime.datetime.fromtimestamp(timestamp, datetime.UTC).
  date = datetime.utcfromtimestamp(weather_data['dt']).date()
{'coord': {'lon': 72.8479, 'lat': 19.0144}, 'weather': [{'id': 721, 'main': 'Haze', 'description': 'haze', 'icon': '50n'}], 'base': 'stations', 'main': {'temp': 303.14, 'feels_like': 306.37, 'temp_min': 303.14, 'temp_max': 303.14, 'pressure': 1010, 'humidity': 62, 'sea_level': 1010, 'grnd_level': 1009}, 'visibility': 2500, 'wind': {'speed': 1.54, 'deg': 90}, 'clouds': {'all': 40}, 'dt': 1729709602, 'sys': {'type': 1, 'id': 9052, 'country': 'IN', 'sunrise': 1729731936, 'sunset': 1729773581}, 'timezone': 19800, 'id': 1275339, 'name': 'Mumbai', 'cod': 200}
{'coord': {'lon': 80.2785, 'lat': 13.0878}, 'weather': [{'id': 701, 'main': 'Mist', 'description': 'mist', 'icon': '50n'}], 'base': 'stations', 'main': {'temp': 302.23, 'feels_like': 309.03, 'temp_min': 301.48, 'temp_max': 303.14, 'pressure': 1010, 'humidity': 84, 'sea_level': 1010, 'grnd_level': 1008}, 'visibility': 4000, 'wind': {'speed': 2.06, 'deg': 240}, 'clouds': {'all': 40}, 'dt': 1729709408, 'sys': {'type': 2, 'id': 2093220, 'country': 'IN', 'sunrise': 1729729836, 'sunset': 1729772115}, 'timezone': 19800, 'id': 1264527, 'name': 'Chennai', 'cod': 200}
{'coord': {'lon': 77.6033, 'lat': 12.9762}, 'weather': [{'id': 301, 'main': 'Drizzle', 'description': 'drizzle', 'icon': '09n'}, {'id': 501, 'main': 'Rain', 'description': 'moderate rain', 'icon': '10n'}], 'base': 'stations', 'main': {'temp': 295.25, 'feels_like': 295.89, 'temp_min': 293.88, 'temp_max': 295.95, 'pressure': 1012, 'humidity': 91, 'sea_level': 1012, 'grnd_level': 911}, 'visibility': 5000, 'wind': {'speed': 2.06, 'deg': 0}, 'rain': {'1h': 1.31}, 'clouds': {'all': 75}, 'dt': 1729709401, 'sys': {'type': 1, 'id': 9205, 'country': 'IN', 'sunrise': 1729730472, 'sunset': 1729772763}, 'timezone': 19800, 'id': 1277333, 'name': 'Bengaluru', 'cod': 200}
{'coord': {'lon': 88.3697, 'lat': 22.5697}, 'weather': [{'id': 500, 'main': 'Rain', 'description': 'light rain', 'icon': '10n'}], 'base': 'stations', 'main': {'temp': 299.12, 'feels_like': 299.12, 'temp_min': 299.12, 'temp_max': 299.12, 'pressure': 1008, 'humidity': 89, 'sea_level': 1008, 'grnd_level': 1007}, 'visibility': 2800, 'wind': {'speed': 4.12, 'deg': 30}, 'rain': {'1h': 0.49}, 'clouds': {'all': 75}, 'dt': 1729709431, 'sys': {'type': 1, 'id': 9114, 'country': 'IN', 'sunrise': 1729728410, 'sunset': 1729769658}, 'timezone': 19800, 'id': 1275004, 'name': 'Kolkata', 'cod': 200}
{'coord': {'lon': 78.4744, 'lat': 17.3753}, 'weather': [{'id': 721, 'main': 'Haze', 'description': 'haze', 'icon': '50n'}], 'base': 'stations', 'main': {'temp': 295.38, 'feels_like': 295.83, 'temp_min': 295.38, 'temp_max': 295.88, 'pressure': 1012, 'humidity': 83, 'sea_level': 1012, 'grnd_level': 955}, 'visibility': 5000, 'wind': {'speed': 2.06, 'deg': 0}, 'clouds': {'all': 20}, 'dt': 1729709447, 'sys': {'type': 1, 'id': 9214, 'country': 'IN', 'sunrise': 1729730496, 'sunset': 1729772321}, 'timezone': 19800, 'id': 1269843, 'name': 'Hyderabad', 'cod': 200}
C:\Users\DELL\weatherMonitor.py:46: DeprecationWarning: The default date adapter is deprecated as of Python 3.12; see the sqlite3 documentation for suggested replacement recipes
  cursor.execute('''INSERT INTO daily_summaries (date, avg_temp, max_temp, min_temp, dominant_condition)

  
Date: 2024-10-23
Average Temp: 25.90°C
Max Temp: 29.99°C
Min Temp: 22.10°C
Dominant Condition: Haze

As well as we get a graphical representation this output as we use the matplotlib to do this.//that has been added in the file section
