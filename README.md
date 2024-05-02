docker pull ghcr.io/home-assistant/home-assistant:stable


docker run -d \
  --name homeassistant \
  --restart=unless-stopped \
  --privileged \
  -e TZ=MY_TIME_ZONE \
  -v /PATH_TO_YOUR_CONFIG:/config \
  -v /run/dbus:/run/dbus:ro \
  --network=host \
  ghcr.io/home-assistant/home-assistant:stable