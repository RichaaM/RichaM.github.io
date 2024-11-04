---
layout: page
title: Optical force feedback 
description: for endoscopic dissection 
img: assets/img/beams_autofbg/pic.png
importance: 2
category: work
related_publications: 
---

This is one of my project (last) as an undergraduate student within the [BEAMS](https://beams.polytech.ulb.be/) (Bio- Electro- And Mechanical Systems) at the Université libre of Bruxelles under [Pr. Alain Delchambre](https://www.linkedin.com/in/alain-delchambre/?originalSubdomain=be).


**Background**

Endoscopic submucosal dissection is a minimally invasive procedure to remove a tumor from the gastrointestinal tract. This special operation uses an electrosurgical knife that applies a high-frequency, high-voltage current to cut the biological tissue at the submucosal level. However, this difficult procedure requires great care not to perforate the muscularis and limit the operation to the mucosal and submucosal region and represents a steep learning curve for practitioners. We could try to provide a force feeback mechanism to monitor in real-time the applied force but the operating conditions, such as the strict dimensional constraints (~2.7mm) or high temperature due to current, do not allow the practical use of traditional force sensors. The current work aims to use fiber Bragg grating (FBG) based strain sensors to take advantage of their sensitivity to strain and temperature. Specifically, the applied strain is reflected by an optical response via a shift in the Bragg wavelength in a nonlinear relationship. This could allow tip force feedback for a closed-loop force control.

<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/beams_autofbg/motivation.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

**Development**

In order to find the non-linear relationship between the wavelength shift provided by the FBG interrogator and the resulting applied force, a calibration testbed is required to gather experimental data. However, manual calibration (accross tip positions, orientation, force levels) took 2 to 3 days of experiments. Such design needed fast iterations so I built a data collection and calibration test-bed using high-precision stepper motors to vary the intensity of the applied force and the orientation (loading and unloading). 

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.html path="assets/img/beams_autofbg/setup.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="caption">
    Hardware set-up composed of actuated linear and rotational stages from Thorlabs and custom 3D-printed parts. The set-up itself would recalibrate after each run with set references. The Fiber-Bragg Grating (FBG) sensor used an FBG-scan 9804 scanner to capture the optical lines data. A precision balance scale recorded weight measurements.
</div>

I configured and developed the calibration procedures, the whole motion control system, and synchronous data collection in C/C++. A critical aspect was preserving the integrity of the sensitive tool which required substantial safeguards on the motion control system.


<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/beams_autofbg/process.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Snapchot of the high-level loop running onboard.
</div>


**Results**

As the table shows, testing and calibrating designs went from 2-3 full days of experiments to a single hour worst case (~30min). The accuracy of measurements improved bu two orders of magnitude. Note that static calibration was now truly enabled since reaching steady-state was impossible manually. I also built an easy-to-use interface using Qt in C++ to configure the hardware and launch and monitor experiments in real-time.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/beams_autofbg/result.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="caption">
    Experiments went down from 2-3 days to under an hour and accuracy improved by 2 orders of magnitude.
</div>


<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/beams_autofbg/auto_fbg1.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/beams_autofbg/auto_fbg3.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

