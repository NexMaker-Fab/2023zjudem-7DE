### What is laser cutting ?

Laser cutting is the process of shining a laser onto a material to melt or burn a narrow controlled strip of material, removing required parts from a blank sheet or slab of material. Power and light frequency defines the capabilities of laser-cutting machines. Generally, a laser cutter includes a “transport” mechanism for the material, the optics, or a combination of the two.
### Materials

Laser cutting technology has advanced significantly, enabling the processing of materials previously deemed challenging. In contemporary home workshops, laser cutters with moderate power, typically up to a few hundred watts, are now commonplace. Even the most formidable materials, like stainless steel, can be cleanly cut using the appropriate techniques.

From modest machines costing under $100 to larger ones capable of cutting steel up to 100 mm thick at speeds of 100 mm/s, the range of laser cutters available is diverse. These lower-cost machines excel at cutting thin sheets and engraving on a wide variety of materials, while the larger machines tackle heavier tasks with precision.

Despite the improved capability of laser cutters, there are still good and bad materials for laser cutting, for example: acrylic, plywood, and MDF. Listed below are the most common laser cutting materials -

- <b><a href="https://www.elecrow.com/blog/acrylic-laser-cutting-all-you-need-to-know.html">Acrylic</a></b>
<div style="text-align:center">
<img src="img/lasercut/acrylic_meta.jpeg" width="100%" height="30%">
</div>
<br>
Known for its exceptional strength, optical clarity, and rigidity, acrylic (PMMA) stands out as a transparent plastic material. There are two variants: cast and extruded. The extruded sheet, although tougher to cut due to residual stresses causing stress cracking, yields better-looking edges at slower cutting speeds. Adequate ventilation is essential during the laser cutting of acrylic due to ignition risk and the toxicity of the resulting vapor.
For cutting acrylic, CO2 or diode-pumped lasers are recommended, emphasizing the use of lower power to avoid scorching. Optimal results occur with an 80 W laser cutting 8 mm acrylic at approximately 5 mm/s, delivering high-quality edges with minimal heat-affected zones (HAZ). Setting the blower to a pressure akin to the strength of blowing on one's finger facilitates proper setup.

- <b><a href="https://www.spp.co.uk/thin-laser-plywood">Plywood</a></b>
<div style="text-align:center">
<img src="img/lasercut/plywood_meta.png" width="100%" height="30%">
</div>
<br>
Derived from bonded wood veneers, plywood, although available in various forms, is universally laser-cuttable. However, the resin bonding emits toxic gases when heated, necessitating ventilation during cutting.
Plywood demands high power and swift speeds during multiple cuts, potentially resulting in an increased kerf size. Enhanced blower pressure facilitates cleaner cutting and supports higher feed rates. CO2 and fiber lasers are the recommended types for plywood cutting.

- <b>Cardboard</b>
<iframe width="560" height="315" src="https://www.youtube.com/embed/uxBf-w9LMEo?si=vcmeMIulPb0ypHG1" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
A widely used material for packaging and modeling, cardboard, despite generating low combustion products and displaying minimal toxicity, benefits from maintained ventilation during laser cutting. Moderate power levels and rapid feed speeds are recommended for cardboard. Controlled blower pressure enhances cut quality while limiting kerfing and heat-affected zones (HAZ).




### Design Rules and Kerf 
Designing for laser cutting involves considering specific rules to ensure accurate and precise results. Additionally, understanding the concept of kerf is crucial in laser cutting design. Here are the design rules and an explanation of kerf:

<h2>Design Rules for Laser Cutting:</h2>

- <b>Vector Graphics:</b> Designs for laser cutting should be in vector format (e.g., SVG, AI, DXF). Vector graphics define shapes and lines using mathematical equations, ensuring scalability without loss of quality.

- <b>Closed Paths:</b> Ensure that all shapes are closed paths without any intersecting lines or open ends. Closed paths define the boundaries for laser cutting, allowing the laser to follow precise cutting paths.

- <b>Line Thickness:</b> Set the line thickness in the design software to match the desired cutting or engraving specifications. Different line colors or layers can signify distinct operations (cutting, engraving, scoring).

- <b>Minimum Features:</b> Maintain a minimum feature size in the design to ensure the laser cutter can accurately reproduce intricate details. This depends on the laser cutter's precision capabilities.

- <b>Overlap for Connections:</b> When designing interlocking parts or connections, add a slight overlap or tolerance between components to ensure a snug fit after cutting.

- <b>Text Orientation:</b> Ensure that any text or labels are in the correct orientation for cutting or engraving. Double-check the orientation to prevent unintended mirrored or upside-down text.

- <b>Bleed and Margin:</b> Incorporate a bleed area (extra space beyond the design) and margins (distance from the edge) to accommodate any material variations and ensure the laser cuts within the intended area.

### Practice laser cut design

We use LaserCAD software to design 2D model. 

> 2D design in LaserCAD software
<br>

<img src="img/lasercut/laserd_1.png">
<img src="img/lasercut/laserd_2.png">
<img src="img/lasercut/laserd_3.png">
<img src="img/lasercut/laserd_4.png">
<img src="img/lasercut/laserd_5.png">
<img src="img/lasercut/laserd_6.png">

<h2>Using of machine </h2>
<br>

>Open the machine
<br>

<img src="img/lasercut/lasercut_1.jpg">
<br>

>Load the material (we use 3mm Acrylic)
<br>

<img src="img/lasercut/lasercut_2.jpg">
<br>

>Turn on the main switch
<br>

<img src="img/lasercut/lasercut_3.jpeg">
<br>

> Make  sure turn on the power for smoke exhaust fan.
<br>

<img src="img/lasercut/lasercut_smoke_adjust.jpeg">

>To adjust laser nozzle use these button
<br>

<img src="img/lasercut/lasercut_4.jpeg">
<br>

> Now load the file (.dxf) from your laptop by using USB.After connect the USB go to select mode on LaserCad Software and download document, then the file will be load into the machine.
<br>

>Set the origin
<br>

<img src="img/lasercut/lasercut_5.jpeg">
<br>

>Set the box
<br>

<img src="img/lasercut/lasercut_6.jpeg">
<br>

For more details to ready the machine in our lab visit <a href="https://www.nexmaker.com/doc/6laser_cutter/Machine_practice.html"> Nexmaker</a>

>Cutted parts
<br>

<img src="img/lasercut/prac_lasercut_1.jpeg">
<img src="img/lasercut/prac_lasercut_2.jpeg">
<img src="img/lasercut/prac_lasercut_3.jpeg">
<br>

> The result of cutting (3mm Acrylic)

| Power/Speed | 10 | 20 | 30 | 40 | 50 | 60 |  |
| -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- |
| 10   | NO   | NO   | NO   | NO   | NO   | NO   |    |
| 20   | YES  | NO  | NO  | NO  | NO  | NO  |   |
| 30  | YES  | YES  | YES  | NO  | NO  | NO  |   |
| 40  | YES  | YES  | YES  | YES  | NO  | NO  |   |
| 50  | YES  | YES  | YES  | YES  | NO  | NO  |   |
| 60  | YES  | YES  | YES  | YES  | YES  | NO  |   |
| 70  | YES  | YES  | YES  | YES  | YES  | NO  |  |
| 80  | YES  | YES  | YES  | YES | YES  | YES  |   |


<br>

### Kerf 

<img src="img/lasercut/kerf.png">
<img src="img/lasercut/kerf_2.jpg">
<br>

After process,we measure the size is 46.75 mm,<br>
so the kerf is kerf= (50-46.75)/10=0.325 mm.

### Assemble laser cut

>Design
<br>

<img src="img/lasercut/lasercut_assemble_design.png">

<video align="centre" width="100%" height="100%" controls muted>
  <source src="img/lasercut/lasercut_assemble.mp4" type="video/mp4">
</video>
<br>

### Arduino Project with laserCAD

We have done one arduino project in arduino section called <a href="https://nexmaker-fab.github.io/2023zjudem-7DE/#/arduino/arduino?id=ir-remote-controlled-led-panel">IR Remote-Controlled LED Panel</a>. So now we have added laser cutting with that project.

We can control the light of different wall of the above assembled laser cutted box.

<img src="img/lasercut/lasercut_witharduino.jpeg">
<br>
<br>
<video align="centre" width="100%" height="100%" controls muted>
  <source src="img/lasercut/lasecut_witharduino_video.mp4" type="video/mp4">
</video>
<br>
<br>
<br>
<video align="centre" width="100%" height="100%" controls muted>
  <source src="img/lasercut/lasercut_arduino_video.mp4" type="video/mp4">
</video>
<br>






























