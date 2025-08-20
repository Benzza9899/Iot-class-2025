# Exploring MQTT QoS Levels

Experiment with QoS 0, 1, and 2.
Observe how message delivery changes based on QoS settings.

## Publisher_qos.py output

```
PS C:\IOT\Iot-class-2025-gateway\app> & C:/IOT/.venv/Scripts/Activate.ps1
(.venv) PS C:\IOT\Iot-class-2025-gateway\app> python .\publisher_qos.py                                            
C:\IOT\Iot-class-2025-gateway\app\publisher_qos.py:20: DeprecationWarning: Callback API version 1 is deprecated, update to latest version
  client = mqtt.Client()
[15:30:21] DEBUG | Sending CONNECT (u0, p0, wr0, wq0, wf0, c1, k60) client_id=b''
Enter message to publish: [15:30:21] DEBUG | Received CONNACK (0, 0)
[15:31:21] DEBUG | Sending PINGREQ
[15:31:21] DEBUG | Received PINGRESP
Hello
Enter QoS level (0, 1, 2): 2
[15:31:41] DEBUG | Sending PUBLISH (d0, q2, r0, m1), 'b'test/qos/6510301017/temperature'', ... (5 bytes)
[15:31:41] PUBLISH REQUESTED | QoS=2 | Message='Hello' | msgid=1
Enter message to publish: [15:31:41] DEBUG | Received PUBREC (Mid: 1)
[15:31:41] DEBUG | Sending PUBREL (Mid: 1)
[15:31:41] DEBUG | Received PUBCOMP (Mid: 1)
[15:31:41] PUBLISHED | msgid=1
```

## Subscriber_qos.py Output

```
(.venv) PS C:\IOT> & C:/IOT/.venv/Scripts/python.exe c:/IOT/Iot-class-2025-gateway/app/subscriber_qos.py
c:\IOT\Iot-class-2025-gateway\app\subscriber_qos.py:25: DeprecationWarning: Callback API version 1 is deprecated, update to latest version
  client = mqtt.Client()
[15:29:26] DEBUG | Sending CONNECT (u0, p0, wr0, wq0, wf0, c1, k60) client_id=b''
[15:29:26] DEBUG | Received CONNACK (0, 0)
[15:29:26] Connected with result code 0
[15:29:26] DEBUG | Sending SUBSCRIBE (d0, m1) [(b'test/qos/6510301017', 2)]
[15:29:26] DEBUG | Received SUBACK

```