# Apple-Coding-Assessment-Exercise

                 # Weather Forecast Application

This Ruby on Rails web application allows users to check the weather forecast for a specific address. The application fetches weather data from the OpenWeatherMap API, provides caching functionality for improved performance, and displays an indicator if the result is pulled from the cache.

## Requirements

- Ruby 3.1.3
- Rails 7.0.4
- OpenWeatherMap API key (sign up at [https://openweathermap.org/api](https://openweathermap.org/api) to  obtain an API key)

## Ruby Version

This application is developed using Ruby version 3.1.3 Please ensure that you have the correct Ruby version installed.

## System Dependencies

Ensure you have the required system dependencies installed. You may need to install additional packages depending on your system configuration.

## Gem Dependencies

This application uses the following Ruby gems:

- [Geocoder](https://github.com/alexreisner/geocoder): A gem for location-based features.
- [HTTParty](https://github.com/jnunemaker/httparty): A gem for making HTTP requests.
- [ActiveSupport](https://guides.rubyonrails.org/active_support_core_extensions.html): Part of the Rails framework, provides utility functions and extensions.
- [dotenv-rails](https://github.com/bkeepers/dotenv): A gem for managing environment variables (used in development and test environments).

To install these gems and their dependencies, add the following lines to your `Gemfile`:

# Geocoder gem for location-based features
gem 'geocoder'

# HTTParty for making HTTP requests
gem 'httparty'

# ActiveSupport for utility functions and extensions
gem 'activesupport'

# Dotenv for managing environment variables (development and test environments)
gem 'dotenv-rails', groups: [:development, :test]

After adding these lines to your Gemfile, run the following command to install the gems:
 bundle install

## Configuration

# Create a GitHub Account:
If you don't have a GitHub account, sign up for one at https://github.com/.
 
 # Create a New Repository:
Log in to your GitHub account.
Click on the '+' icon in the upper right corner and select "New repository."
Fill in the repository name, description, and other details.
Choose the visibility (public or private) for your repository.
Click the "Create repository" button.

# Clone the Repository:

On the repository page, click the "Code" button and copy the repository URL.
Open your terminal or command prompt and navigate to your project directory.

1. Clone the repository to your local machine:
git clone https://github.com/yourusername/weather_app.git

2.cd weather_app

3.Create a .env file in the project's root directory and add your OpenWeatherMap API key:
OPENWEATHERMAP_API_KEY=your_api_key_here

## Services
This application uses services to manage weather-related functionality. Here are the services used in the application:

WeatherService
The WeatherService class is responsible for fetching weather data from the OpenWeatherMap API and checking the cache for cached data.

CityValidator
The CityValidator class is used to validate city names entered by users.

Services help organize the code and provide a modular structure for different components of the application.

## Usage

1.Enter an address in the provided input field and click the "Search" button to retrieve the weather forecast.
2.The application will display the requested forecast details, including the current temperature.
3.If the data is retrieved from the cache, you will see an indicator that it was pulled from the cache.

## Cache Management

Weather forecast data is cached for 30 minutes for all subsequent requests by zip codes.
Cached data is automatically cleared after 30 minutes.
An indicator is displayed when the result is pulled from the cache.

## Application Structure
The application uses a WeatherController to handle user requests.
It checks the validity of the city name using a CityValidator.
Weather data and user input are cached using Rails caching.

## Running Tests
This project includes unit tests written using RSpec. To run the tests, use the following command:
1. rspec spec/services/city_validater_spec.rb
2. rspec spec/services/weather_service_spec.rb
3. bundle exec rspec

