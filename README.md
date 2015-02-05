# myo-spark
Connecting Thalmic Myo with Spark Core for some gesture triggered IoT action.

In this particular case we are triggering a 220V light with the help of our gestures.

#Requirements

- Spark Core
- Thalmic Myo
- Arduino relay shield

#Installation and Useage

- Flash the Spark core with myo-spark-build.io , you should now be able to toggle the pin D0 on/off using the following Spark API :

```
curl https://api.spark.io/v1/devices/[device id here]/led -d access_token=[your access token here] -d params=l1,HIGH

curl https://api.spark.io/v1/devices/[device id here]/led -d access_token=[your access token here] -d params=l1,LOW

```

- Update the myo.py file with your device ID and access token replacing the existing ones.

- Wear the myo , run the myo.py file and perform sync. You should now be able to trigger D0 pin using the fist and wave in gestures.

- Connect the D0 pin to the Arduino relay shield/module and hook up any 110/220V appliance to it.

- If you dont have the relay module/shield you can quickly hack it together with a relay , transistor , resistor and diode as shown in image arduino_relay.jpg

Feel like Iron man , you can now control your house directly from your motor-neurons :)

http://amit.sh