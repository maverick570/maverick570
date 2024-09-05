<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Transport Booking Form</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 20px;
        }
        .container {
            max-width: 800px;
            margin: 0 auto;
            background: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        h1 {
            text-align: center;
            margin-bottom: 20px;
        }
        .form-group {
            margin-bottom: 15px;
        }
        .form-group label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
        }
        .form-group input,
        .form-group select,
        .form-group textarea {
            width: 100%;
            padding: 8px;
            border: 1px solid #ddd;
            border-radius: 4px;
        }
        .form-group input[type="date"] {
            width: calc(50% - 10px);
            display: inline-block;
        }
        .form-group input[type="submit"] {
            background-color: #4CAF50;
            color: white;
            border: none;
            cursor: pointer;
        }
        .form-group input[type="submit"]:hover {
            background-color: #45a049;
        }
        .form-group .half {
            display: inline-block;
            width: calc(50% - 10px);
            margin-right: 10px;
        }
        .form-group .half:last-child {
            margin-right: 0;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Transport Booking Form</h1>
        <form action="/submit-booking" method="post">
            <div class="form-group">
                <label for="name">Full Name:</label>
                <input type="text" id="name" name="name" required>
            </div>
            <div class="form-group">
                <label for="email">Email Address:</label>
                <input type="email" id="email" name="email" required>
            </div>
            <div class="form-group">
                <label for="phone">Phone Number:</label>
                <input type="tel" id="phone" name="phone" required>
            </div>
            <div class="form-group">
                <label for="departure">Departure Location:</label>
                <input type="text" id="departure" name="departure" required>
            </div>
            <div class="form-group">
                <label for="arrival">Arrival Location:</label>
                <input type="text" id="arrival" name="arrival" required>
            </div>
            <div class="form-group">
                <label for="departure-date">Departure Date:</label>
                <input type="date" id="departure-date" name="departure_date" required>
            </div>
            <div class="form-group">
                <label for="return-date">Return Date (Optional):</label>
                <input type="date" id="return-date" name="return_date">
            </div>
            <div class="form-group">
                <label for="transport-mode">Mode of Transport:</label>
                <select id="transport-mode" name="transport_mode" required>
                    <option value="">Select a mode</option>
                    <option value="bus">Bus</option>
                    <option value="train">Train</option>
                    <option value="flight">Flight</option>
                    <option value="car">Car</option>
                </select>
            </div>
            <div class="form-group">
                <label for="additional-info">Additional Information:</label>
                <textarea id="additional-info" name="additional_info" rows="4"></textarea>
            </div>
            <div class="form-group">
                <input type="submit" value="Book Now">
            </div>
        </form>
    </div>
</body>
</html>
