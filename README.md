===== Custom Crazyflie Nano Firmware =====

THIS IS BASED ON THE ORIGINAL BITCRAZE FIRMWARE!

I didn't write most of this code, but copied it from the public repos on the [Bitcraze Bitbucket account](https://bitbucket.org/bitcraze/crazyflie-firmware).

I just made a few modifications so that I get more sensor readings. This firmware is still completely compatible with whatever you might want to do with your quadcopter (as of the time of writing this - 2013/06/03).

What I changed:

* Outputting additional sensor readings
  * `acc` Accelerometer (x, y, z)
  * `gyro` Gyroscope (x, y, z)
  * `mag` Magnetometer (x, y, z)
  * `alti` Altimeter (pressure, temperature)

A few things concerning the sensor values above:
* The pressure comes out as `0` all the time. Got to figure that one out, still.
* The magnetometer readings are not normalized (so you might not be able to use them).

Other that that, just use the readings like you would do with the `stabilizer` log variables (add a block, add the log variables and read them from the incoming packets, etc.).
