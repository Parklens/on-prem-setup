# Cam Server
## Image: gcr.io/parklens/cam-server
## Env Vars:
- GITHUB_TOKEN
- PARKLENS_API_URL
- PARKLENS_PREDICTOR_URL
- LOT_ID
- JWT_PUBLIC_KEY_PATH=jwt/jwt_rsa.pub
- PARKLENS_USER
- PARKLENS_PASSWORD
- PORT
- LOGLEVEL=INFO

# Cam Server Web App
## Image: gcr.io/parklens/cam-server-webapp
## Env Vars:
- REACT_APP_CAM_SERVER_URLS={"server_alias":"http://[server-url]:[port]"}
- REACT_APP_CLOUD_URL=https://api.parklens.com/v2
- REACT_APP_PRIMARY_COLOR=#221F20
- REACT_APP_SECONDARY_COLOR=#496e9b
- REACT_APP_TEXT_COLOR=white
- REACT_APP_LOGO_SRC=https://[logo-url].jpg

# Predictor API 
## Image: gcr.io/parklens/predictor-api
## Env Vars: 
- LOGLEVEL=INFO
- PORT
- REDIS_HOST
- REDIS_PORT
- REDIS_PASSWORD
- GITHUB_TOKEN
- JWT_PUBLIC_KEY_PATH=jwt/jwt_rsa.pub

# Predictor Worker CPU
## Image: gcr.io/parklens/predictor-worker-cpu
## Env Vars:
- LOGLEVEL=INFO
- REDIS_HOST
- REDIS_PORT
- REDIS_PASSWORD
- BATCH_SIZE=64
- REDIS_TIMEOUT=15
- CUDA_VISIBLE_DEVICES='-1'
- MODEL_JSON_FILE=VG_car_model22.json
- MODEL_WEIGHT_FILE=VG_car_model22-39-0.99.h5

# Predictor Worker GPU
## Image: gcr.io/parklens/predictor-worker-gpu
## Env Vars:
- LOGLEVEL=INFO
- REDIS_HOST
- REDIS_PORT
- REDIS_PASSWORD
- BATCH_SIZE=64
- REDIS_TIMEOUT=15
- MODEL_JSON_FILE=VG_car_model22.json
- MODEL_WEIGHT_FILE=VG_car_model22-39-0.99.h5

# Redis 
## Image: redis:5.0.9
## Env Vars: 
- REDIS_PASSWORD=optional


