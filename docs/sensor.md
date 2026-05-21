---
show_toc: true
---

# The Sensor

At the heart of Local Air is a bespoke air quality sensor, designed and built at the University of Bristol to integrate directly into commercial e&#8209;scooter hardware.
{.banner}

The sensor measures multiple air pollutants simultaneously, uploads data in near real-time, and is robust enough to survive the rigours of daily urban use: rain, vibration, temperature extremes, and the occasional knock.

Getting to this point has taken three rounds of iterative development, each one informed by what we learned from the last.

---

## Why low-cost sensors?

Traditional reference-grade air quality instruments are highly accurate but prohibitively expensive, being often tens of thousands of pounds per unit. Deploying them at the scale needed to understand street-level air quality variation across a whole city simply isn't feasible.

Low-cost sensors have changed the picture dramatically. Advances in electrochemical and optical sensing technology mean it is now possible to measure the key urban air pollutants (nitrogen dioxide, particulate matter, carbon monoxide, and others) for around **£300 per unit**. That price point makes city-scale deployment genuinely achievable for the first time.

The trade-off is accuracy: low-cost sensors are not as precise as reference instruments, and they can drift over time. A significant part of the Local Air research programme is developing the data processing techniques needed to correct for these limitations (you can read more about that on the [Data page](data.md)).

---

## Round 1: Proof of concept

<div class="row align-items-center" markdown>
<div class="col" markdown>

The first phase of Local Air sensor development focused on selecting the right sensing technologies and proving that the fundamental approach was feasible. A breadboarded prototype was built to evaluate different sensor options side by side and supported system development.

From this, a small form-factor proof-of-concept device was produced, compact enough to be practically mounted on a scooter, and incorporating the sensing technologies that performed best in the evaluation. This device was never intended for deployment; its purpose was to answer the question of whether the approach could work at all.

The answer was yes.

</div>

<div class="col-lg-3 col-xl-2">
<img src="/images/sensor_first_soldered_1_cutout.png" alt="First sensor prototype" class="d-block mx-auto" style="max-height: 30rem">
</div>
</div>

---

## Round 2: Real-world testing

<div class="row align-items-center" markdown>
<div class="col" markdown>

With the sensing technology selected, attention turned to building something that could survive the real world. Voi, then Bristol's e-scooter fleet operator, provided an e-scooter to the project as a laboratory testbed. This allowed the team to understand exactly how the sensor would need to integrate with the scooter's mechanical and electrical systems.

A purpose-designed enclosure was produced at the University of Bristol using resin-based 3D printing technology, giving a level of precision and weather resistance that would have been impossible with conventional manufacturing at this scale. The enclosure was designed so that the sensor could be installed and removed simply, minimising the time and expertise required for deployment and maintenance.

This version of the sensor was tested in Bristol, mounted on the lab scooter and ridden through the city to gather initial real-world data. The results were encouraging, the sensor performed as expected, and the enclosure held up well to the conditions.

</div>

<div class="col-lg-5">
<img src="/images/Populated_in_case_14.jpg" alt="Second sensor prototype, attached to a Voi e-scooter" class="d-block mx-auto" style="max-height: 30rem">
</div>
</div>

---

## Round 3: Deployment ready

<img src="/images/Labelled_Diagram_of_Sensor.png" alt="Third sensor prototype, attached to a Voi e-scooter. Showing sensors highlighted: 1. Carbon monoxide, nitrogen dioxide, ethyl alcohol and volatile organic compounds. 2. Particulate matter (PM1, PM2.5, and PM10). 3. Temperature and humidity. 4. Ambient noise." class="d-block mx-auto mb-3">

The third round of development produced the sensor used in the [London deployment](deployment.md): a fully integrated, deployment-ready unit designed for installation across a commercial fleet. Ten of these units were manufactured and deployed in London, where they operated for three months and gathered over a million air quality readings.

The Round 3 sensor measures the following pollutants and environmental parameters:

| Parameter                             | Measurement technology     |
|---------------------------------------|----------------------------|
| Nitrogen dioxide (NO₂)                | Electrochemical            |
| Carbon monoxide (CO)                  | Electrochemical            |
| Volatile Organic Compounds (VOC)      | Electrochemical            |
| Particulate matter (PM1, PM2.5, PM10) | Optical (laser scattering) |
| Temperature                           | Solid state                |
| Relative humidity                     | Solid state                |
| Ambient acoustic noise                | MEMS microphone            |

---

## Round 4: What's next

We are now seeking funding to carry out a large-scale deployment in Bristol, scaling up from 10 sensors to 100 and extending the data collection period to three years. This next phase will also involve a redesign of the sensor to integrate with Dott's (who now operate the e-scooter fleet in Bristol) updated vehicle, building on everything learned in the previous three rounds of development.

If you're interested in supporting or partnering with this work, [get in touch](team.md#contact-us-and-get-involved).

---

## Innovations

### Acoustic noise sensing for source identification

One of the challenges of air quality monitoring is understanding not just *how much* pollution is present, but *where it is coming from*. Identifying pollution sources (whether that's a busy junction, an idling delivery vehicle, or a particular industrial premises) is essential for targeting interventions effectively.

The Local Air sensor includes a MEMS microphone that continuously measures ambient acoustic noise levels (this essentially gives a single value saying "how loud it is", does not allow voices to be identified, or even heard). Traffic noise is a strong proxy for traffic volume and type, and by correlating acoustic data with pollutant readings, it becomes possible to begin attributing pollution spikes to specific sources. This capability is built into every unit at no additional cost.

### On-board data encryption

All data stored on the sensor's internal SD card is encrypted using SPEC encoding before it is written to storage. This means that even if a sensor is lost or stolen, the data it contains cannot be read without the encryption key. Raw data is never stored in an unencrypted form on the device. This approach to data security is particularly important given that the sensors operate in public spaces on vehicles that are accessible to members of the public.
