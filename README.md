# Dockerfile for Recommendation System

This Dockerfile sets up a container for a recommendation system using Flask, Surprise, and other libraries.

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/yourrepository.git
   ```

2. Build the Docker image:

   ```bash
   docker build -t recommendation-system .
   ```

3. Run the Docker container:

   ```bash
   docker run -d -p 5000:5000 recommendation-system
   ```

## Usage

To use the recommendation system, send HTTP requests to the API endpoints:

- `/recommend` for personalized recommendations
- `/general_recommend` for general recommendations
- `/user_history_recommend` for user-specific recommendations based on past purchases
- `/user_preferences_recommend` for user-specific recommendations based on preferences
- `/popular_products` for popular products
- `/new_products` for new products

Example request:

```bash
curl -X POST http://localhost:5000/recommend -H "Content-Type: application/json" -d '{"user_id": 123, "product_id": 456, "num_recommendations": 5}'
```

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request.

## License

This project is licensed under the MIT License 
