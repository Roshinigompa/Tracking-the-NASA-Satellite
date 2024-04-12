# Tracking-the-NASA-Satellite

This project aims to track the location of the NASA satellite in real-time using streaming data provided by NASA. The data is obtained from the following endpoint:

 **Endpoint:** [http://api.open-notify.org/iss-now.json](http://api.open-notify.org/iss-now.json)

The data is in JSON format and includes the timestamp, latitude, and longitude of the International Space Station (ISS) at the time of the request.

## Requirements

To run the project, you'll need:

- Python 3.x
- Libraries: requests, matplotlib, basemap

## Installation

1. Clone the repository:

    ```
    git clone https://github.com/your_username/ISS-Tracker.git
    ```

2. Navigate to the project directory:

    ```
    cd ISS-Tracker
    ```

3. Install the required dependencies:

    ```
    pip install -r requirements.txt
    ```

## Usage

To track the NASA satellite, follow these steps:

1. Run the producer script to start streaming data:

    ```
    python producer.py
    ```

   The producer will run for an hour, fetching data from the NASA API at 5-second intervals.

2. Run the consumer script to visualize the satellite's location:

    ```
    python consumer.py
    ```

   This script will fetch the streaming data from the producer and plot the satellite's location on the world map. The map will continuously update every 5 seconds to show the satellite's movement over the hour.

## Note

- The satellite moves quickly, so the graph may show more than half of the map covered with the satellite track.
- Ensure a stable internet connection to fetch real-time data from the NASA API.


