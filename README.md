Food Log Web Application

This project implements a web application for tracking daily food intake using SQLite and Flask. Users can log their meals with details on protein, carbohydrates, fat, and total calories. The application allows users to view their food logs by date and add new food items to the database.

Table Structure
log_date

    id: Integer (Primary key, Autoincrement)
    entry_date: Date (Not null)

food

    id: Integer (Primary key, Autoincrement)
    name: Text (Not null)
    protein: Integer (Not null)
    carbohydrates: Integer (Not null)
    fat: Integer (Not null)
    calories: Integer (Not null)

food_date

    food_id: Integer (Not null)
    log_date_id: Integer (Not null)
    Primary Key: (food_id, log_date_id)

Usage

    Homepage (/): Displays a summary of daily food intake including total protein, carbohydrates, fat, and calories. Users can add new dates for logging meals.

    View Specific Date (/view/<date>): Allows users to view and add food items consumed on a specific date. Shows cumulative totals for protein, carbohydrates, fat, and calories consumed that day.

    Add Food (/food): Enables users to add new food items to the database with details on protein, carbohydrates, fat, and automatically calculates total calories.

Installation

    Clone the repository:

    bash

git clone https://github.com/your_username/food-log-web-app.git
cd food-log-web-app

Install dependencies:

pip install -r requirements.txt

Run the application:

    python app.py

    Open the application in your web browser: http://localhost:5000

Dependencies

    Flask
    SQLite3

Contributing

Contributions are welcome! Please feel free to open issues or pull requests.
License

This project is licensed under the MIT License - see the LICENSE file for details.
