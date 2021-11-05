### Starting MongoDB

Run

```
docker volume create data-mongodb
```

and then

```
docker run -v data-mongodb:/data/db -p 27017:27017 --name mongodb -d mongo
```

### Starting Kafka

Run

```
docker-compose up -d
```

in the root directory.

### Install Dependencies

```
pip install -r requirements.txt
```

### Run the threads

Before running, you have to start MongoDB and Kafka as described above.

#### Run Producer Application

```
python producer_app.py
```

#### Run Consumer Application

```
python consumer_app.py
```
