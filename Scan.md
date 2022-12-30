# Scan for Network(s)

Use MicroPython on PRi Pico W to scan for network(s).

## Code

``` python
# https://docs.micropython.org/en/latest/library/network.WLAN.html

# Import module
import network

# Configure Pico W as a client
wlan = network.WLAN(network.STA_IF)

# Scan for networks
networks = wlan.scan()  # List of tuples

# Display results for each network
for network in range(len(networks)):
    print("SSID:", networks[network][0])
    print("bSSID:", networks[network][1])
    print("Channel:", networks[network][2])
    print("RSSI:", networks[network][3])
    print("Security:", networks[network][4])
    print("Hidden:", networks[network][5], "\n")

```
