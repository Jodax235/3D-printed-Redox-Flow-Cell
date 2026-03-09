# 3D-printed open-source Redox-Flow-Cell

`This is both a documentation of and a guide to a low-cost, fully 3D-printed redox-flow-cell that operates using charge-dependent color-changing electrolytes, demonstrating the general principle behind this future technology of energy storage. The cell serves as a test carrier and is ideal for own experiments with the technology.`

# 0. Disclaimers

**License**

3D-printed-Redox-Flow-Cell © 2024 by [Jonathan Danner](https://www.linkedin.com/in/jonathan-danner-77b531230/) is licensed under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)

**Prototype Status and No Guarantee of Performance**

The cell described in this project is a research prototype. Although it has demonstrated functional performance under our specific experimental conditions, it may contain design limitations, manufacturing tolerances, or operational constraints that have not been fully identified or resolved. Successful replication and operation require precise fabrication, careful assembly, and controlled handling. Variations in materials, equipment, environmental conditions, or user expertise may significantly affect performance and safety. Accordingly, no representation or warranty is made regarding the functionality, reliability, durability, safety, or suitability of the cell when constructed or operated by third parties, even if the provided instructions are followed. Users acknowledge that experimental systems inherently involve uncertainty and assume full responsibility for verification, validation, and risk assessment prior to any implementation or use.

**Safety Notice and Disclaimer (Open Source Hardware Documentation)**

This documentation describes the design, construction, and operation of a 3D-printed redox flow cell and related components. The project involves electrical systems, reactive chemicals, and laboratory procedures that may present significant hazards, including but not limited to electric shock, fire, chemical burns, toxic exposure, environmental harm, serious injury, or death. This material is provided for informational and educational purposes only. Any use, reproduction, modification, or implementation of the described designs and procedures is undertaken entirely at the user’s own risk. This project is intended exclusively for qualified professionals with appropriate training in electrical systems, chemical handling, and laboratory safety. Proper facilities, certified safety equipment, and competent supervision are required. Users are solely responsible for ensuring compliance with all applicable local, national, and international laws, regulations, safety standards, and environmental requirements. 

THE AUTHORS, CONTRIBUTORS, AND DISTRIBUTORS PROVIDE THIS DOCUMENTATION “AS IS,” WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE, AND NON-INFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR CONTRIBUTORS BE LIABLE FOR ANY CLAIM, DAMAGES, LIABILITY, OR OTHER LOSS ARISING FROM OR RELATED TO THE USE, MISUSE, OR INABILITY TO USE THE INFORMATION PROVIDED.

# 1. Introduction & Epilogue

We - a group of three high school students from Germany - originally started this project as part of the German youth science competition “jugend forscht” (”youth experiments”), where the project won the chemistry category in the regional competition in Brunswick and proceeded to score 4th place in the state competition of Lower Saxony.

Our goal was to apply the possibilities of advancing consumer 3D-printing to the still new technology of redox-flow-cells in order to create a comparatively easy-to-produce test carrier, which could be used as a base for broader experimenting with the technology, even at an amateur level. The three main applications of the test carrier - among others - were thought to be:

1. Use for educational purposes in educational institutions to better convey the concept of redox-flow-cells

2. Simplified testing of electrolytes or parts surrounding the main cell, for which a simple placeholder is needed

3. Allowing amateurs to experiment with the technology in private settings

In order to allow for such use scenarios and to better convey the principle of a redox-flow-cell, the electrolytes chosen - anthraquinone disulfone (ACDS) and potassium hexaferricyanide - have the ability of charge-state dependent color-change, altering their color while the cell is being charged, indicating the inner dynamics of the technology. Furthermore, both anthraquinone disulfone (ACDS) and potassium hexaferricyanide are particularly suitable for the applications specified above, as they are less chemically corrosive than other more regularly used electrolytes and therefore safer/easier to operate in less professional settings. 
In theory however, the cell does allow for the use of other electrolytes as well (see below for “Material selection and compatibility testing”).

Mainly due to constraints in time, resources, and technical equipment, we never managed to complete the project to its full potential. Major starting points for future work would firstly be an improvement of the overall leak tightness of the system, especially in the joint between the cells and membrane. Although the cell has proven to work accordingly even under demanding conditions, the system’s leak tightness requires a very large clamping force, resulting in high material stress on the cell’s main structure and lowering the cell’s life expectancy. One suitable variable already identified are the rubber gaskets - replacing the commercial-grade parts currently in use with more suitable industrial-grade ones seems to be a promising starting point. 

Secondly, the cell was only ever tested with one pair of electrolytes. A comparison between different electrolytes under accurately comparable conditions would be interesting to see. For the spectrum of electrolytes already or potentially compatible with the cell, see below. 

Thirdly, an array of already pre-tested and well documented electric consumer ready to be used for the cell would facilitate both the educational and private experimental-capabilities of the cell.

Fourthly, it could be tested whether the cell might work with other types of membranes, either without a loss in efficiency or at a cost. The membrane currently in use is a Nafion N-117 membrane, which is a semipermeable cation exchange membrane. Changing the type of membrane used might severely reduce cost, as the membrane is currently by far the most expensive single part of the entire cell, attributing to more than half of the total cost.

# 2. A short Introduction into Redox-Flow-Cells

![image.png](attachment:64868ee5-6306-4c2f-afb1-6c18a21036fb:image.png)

![images.jpeg](attachment:e5ed0d87-4ff2-40cb-a88d-621d381d6334:images.jpeg)

A redox flow battery consists of two electrolyte tanks and the electrochemical cell itself, which is divided into two half-cells by a semipermeable membrane. Using pumps, two electrolytes (or a single electrolyte in different oxidation states) are circulated along the membrane within separate flow circuits. According to the conventional direction of current, electrons flow from the cathode to the anode during the charging process. As a result, an electron deficiency develops at the cathode, which attracts negative charge carriers, while an electron surplus forms at the anode, attracting positive charge carriers. A supporting electrolyte (conducting salt), added in advance, is essential for enabling ionic conductivity. The ions contained in this electrolyte balance the charge difference by migrating from the positively charged side to the negatively charged side through the membrane. Driven by the applied voltage, the more positive electrolyte continuously releases electrons at the cathode and is therefore oxidized, while the more negative electrolyte accepts electrons at the anode and is consequently reduced. In this altered charge configuration, the supplied electrical energy is stored chemically within the electrolytes. If the flow direction of the pumps is reversed, the reverse reaction occurs and the cell is discharged. Because this reaction proceeds spontaneously, it does not require an external electrical input (apart from the energy needed to operate the pumps). Instead, electrical energy is released. During discharge, the previously oxidized electrolyte is reduced and the previously reduced electrolyte is oxidized, returning both to their original chemical states. However, when the electrolytes are dissolved in distilled water, unwanted side reactions with the solvent may occur during the reverse reaction, leading to the formation of hydrogen gas. As a consequence, the reaction cannot proceed completely, and the initially supplied energy cannot be fully recovered. Nevertheless, redox flow batteries represent an attractive option for energy storage, among other reasons because they can operate without ethically problematic charge carriers such as lithium.

# 3. Complete list of parts, equipment, and tools required

## Equipment/tools required for building/operating the cell:

### Electrical Equipment:

| Part | Describtion/Measurements | Number of parts |
| --- | --- | --- |
| Laboratory power supply |   • 2x PSU with one controllable DC-Output **or** • one PSU with two individually controllable DC-Outputs |  |
| Multimeter |   • one amperemeter and one voltmeter **or** • one multi-purpose-sensor-system (e.g. CASSYLAB) with the capabilities specified above |  |
| Cables | standard lab low-voltage power cables with banana plugs | min. 9 (or more, depending on length) |
| Alligator clips  |  | 4 |
| Electronic load (or other energy consumer usable for discharging) | Capable of very low energy consumption (under 1V and 1A) |  |

**Measuring Devices:**

The most basic experimental setup of the cell employs two digital multimeters, one configured as a voltmeter and the other as an amperemeter. It is however highly recommended to use a multi-purpose interface capable of simultaneously recording both voltage and current as well as recording data. While the integration of both measurements into a single device is relevant purely for simplicity, the ability to log and graph data is fundamental to performing evaluable test runs for developing and iterating the cell. Conversely, the mentioned usage of two multimeters is perfectly sufficient for less scientific purposes/experiments. 

### Laboratory Equipment:

| Part | Describtion/Measurements | Number of parts |
| --- | --- | --- |
| Measuring cylinder | capacity ≥ 100 ml | 1 |
| Sealable round-bottom flask | capacity ≥ 100 ml | 2 |
| Beaker or screw-top jar | capacity ≥ 200 ml | 3 |
| Chemical-resistant, sealable container  |  | 1 |
| Precision scale | accurate to at least two decimal places | 1 |
| Weighing pan |  | 3 |
| Spatula |  | 2 |
| Personal Protection Equipment (disposable gloves, safety goggles, lab coat, etc.) |  |  |
| Paper towels |  |  |
| Small brush, toothbrush, etc. |  |  |

### Tools:

Only non-standard tools are listed.

| Part | Describtion/Measurements |
| --- | --- |
| 3D-Printer |  |
| Everything required to post-process 3D-printed parts (e.g. Dremel) |  |
| combination wrench/ring spanner 14mm |  |
| combination wrench/ring spanner 8mm |  |
| Thread cutter (for M5 threads) |  |
| Iron-cutting tools |  |
| Sharp knife |  |
| Calipers |  |
| Marker |  |

## Chemicals required for the cell:

Note: The precise quantities required to prepare the electrolytes are specified below under “Setup of the cell > Preparation of Electrolytes”. These numbers only act as an estimate for purchasing or gathering.

Note: Please check for the correct translation of chemical names beforehand.

| Chemical | Quantity (per run) | Links (Germany) |
| --- | --- | --- |
| Destilled water | 150 ml |  |
| Potassium hexacyanoferrate(II) trihydrate (K₄[Fe(CN)₆] · 3 H₂O) | 10 g | [https://www.carlroth.com/de/en/a-to-z/potassium-hexacyanoferrate(ii)-trihydrate/p/7974.2](https://www.carlroth.com/de/en/a-to-z/potassium-hexacyanoferrate%28ii%29-trihydrate/p/7974.2) |
| Anthraquinone-2,7-disulfonic acid disodium salt (C₁₄H₆Na₂O₈S₂) | 5 g | https://www.carlroth.com/de/en/other-fine-chemicals/anthraquinone-27-disulfonic-acid-disodium-salt/p/2ch2.5 |
| Ammonium sulfate | 5 g | https://www.carlroth.com/de/de/von-a-bis-z/ammoniumsulfat/p/9218.1 |
| Rubbing alcohol (e.g. Ethanol, Isopropanol, Isopropyl) | - |  |

## Parts required for constructing the cell:

| Part | Describtion/Measurements | Number of parts | Direct links (German/Germany) |
| --- | --- | --- | --- |
| Filament | PLA/PETG or better | at least 250-300g | - |
| Copper Plates | 40mm x 40mm x 2mm | 2 | https://www.amazon.de/dp/B09ZB9TKM1?th=1 |
| Graphite Electrode | 40mm x 40mm x 5mm | 2 | https://graphite24.de/products/graphiteplatte_5mm?variant=47499976638794 |
| Graphite fabric | 40mm x 40mm (thickness not relevant) | 2 (per cell, single-use only) | https://www.amazon.de/dp/B0G43SPVTN?th=1 |
| Rubber Gasket | • inner diameter: > 57mm • outer diameter: < 82mm • thickness: min. 2mm | 2 | https://www.hornbach.de/p/epdm-ring-60-x-78-x2-mm-70-sh-a/10257196/ |
| Membrane | Diameter equal to the outer diameter of the used gaskets |  | https://www.fishersci.de/shop/products/nafion-r-n-117-membrane-0-180mm-thick-0-90-meq-g-exchange-capacity-thermo-scientific/11389827 |
| Bolts |   • hex bolt DIN 933 8.8 M5, min. 55mm • hex bolt DIN 933 8.8 M5, ±35mm | 4 each |  |
| Nuts | hex nut DIN 934 8 M5 | 4 |  |
| Screws  | M3 flat head countersunk screw with nuts, min. 16mm long | 4 | https://www.globus-baumarkt.de/p/connex-gewindeschrauben-m3-x-16-mm-ph-1-senkkopf-30-stk-0763023329/ |
| Washers | washer DIN 9021 ID 53mm, OD 92mm | 4 |  |
| Peristaltic pump | Pump mount only works with the linked model. For other pumps, the mount might need to be modified | 1 (double-head) | [https://de.aliexpress.com/item/1005003694510296.html?spm=a2g0o.detail.pcDetailTopMoreOtherSeller.7.1d702wPv2wPvY4&gps-id=pcDetailTopMoreOtherSeller&scm=1007.40050.354490.0&scm_id=1007.40050.354490.0&scm-url=1007.40050.354490.0&pvid=de75b816-1bef-42ad-83b2-f87ef99126ea&_t=gps-id:pcDetailTopMoreOtherSeller,scm-url:1007.40050.354490.0,pvid:de75b816-1bef-42ad-83b2-f87ef99126ea,tpp_buckets:668%232846%238110%231995&pdp_ext_f={"order"%3A"78"%2C"eval"%3A"1"%2C"sceneId"%3A"30050"%2C"fromPage"%3A"recommend"}&pdp_npi=6%40dis!EUR!27.86!26.19!!!31.82!29.91!%40211b613917725314367481306ed3ef!12000027695004168!rec!DE!6996493725!XZ!1!0!n_tag%3A-29919%3Bd%3Aa9c1a3ed%3Bm03_new_user%3A-29895&utparam-url=scene%3ApcDetailTopMoreOtherSeller|query_from%3A|x_object_id%3A1005003694510296|_p_origin_prod%3A](https://de.aliexpress.com/item/1005003694510296.html?spm=a2g0o.detail.pcDetailTopMoreOtherSeller.7.1d702wPv2wPvY4&gps-id=pcDetailTopMoreOtherSeller&scm=1007.40050.354490.0&scm_id=1007.40050.354490.0&scm-url=1007.40050.354490.0&pvid=de75b816-1bef-42ad-83b2-f87ef99126ea&_t=gps-id:pcDetailTopMoreOtherSeller,scm-url:1007.40050.354490.0,pvid:de75b816-1bef-42ad-83b2-f87ef99126ea,tpp_buckets:668%232846%238110%231995&pdp_ext_f=%7B%22order%22%3A%2278%22%2C%22eval%22%3A%221%22%2C%22sceneId%22%3A%2230050%22%2C%22fromPage%22%3A%22recommend%22%7D&pdp_npi=6%40dis%21EUR%2127.86%2126.19%21%21%2131.82%2129.91%21%40211b613917725314367481306ed3ef%2112000027695004168%21rec%21DE%216996493725%21XZ%211%210%21n_tag%3A-29919%3Bd%3Aa9c1a3ed%3Bm03_new_user%3A-29895&utparam-url=scene%3ApcDetailTopMoreOtherSeller%7Cquery_from%3A%7Cx_object_id%3A1005003694510296%7C_p_origin_prod%3A) |
| Silicon Tube |   • ID: 5mm; OD: 8mm • at least 4m (the longer, the easier) |  | [https://www.amazon.de/LAVMHAB-Silikonschlauch-Lebensmitteltaugliche-Schläuche-übertragen/dp/B0DR73B74R/ref=sr_1_3_sspa?dib=eyJ2IjoiMSJ9.hcmdMJ9bJhnsDKF_PG3YyzGQne7--8ZoYi9tPzpFmFpaSdIiBAMVk0maA6Xg0Z07FpGoZ2w7Ol3X76dyf4FMwIpJZ4BIMJtbuPnurizN_iUqS37uUP58o36gFeCerndimjO0C2oagYNmq0NlUv4lTamng7e29GlRTGIIYNLMVV-l6BU_pAyHxgbi-evxixk_2KUtG530UASs1kwiv4Rh_d6fnwmggIUfXCzCwcv1vxhaIWVLRnIPM5cQA0mkdcqjcid_D-KzAsP9pGsqh9u2JViDrAnj2aXfLiYGj7XVGhg.blQv3wklhGlqUeWlj2_1Z03i7PG_JX8J9u94NjVHQYE&dib_tag=se&keywords=silikonschlauch%2B5mm&qid=1772531638&sr=8-3-spons&aref=YRg9eceQvl&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&th=1](https://www.amazon.de/LAVMHAB-Silikonschlauch-Lebensmitteltaugliche-Schl%C3%A4uche-%C3%BCbertragen/dp/B0DR73B74R/ref=sr_1_3_sspa?dib=eyJ2IjoiMSJ9.hcmdMJ9bJhnsDKF_PG3YyzGQne7--8ZoYi9tPzpFmFpaSdIiBAMVk0maA6Xg0Z07FpGoZ2w7Ol3X76dyf4FMwIpJZ4BIMJtbuPnurizN_iUqS37uUP58o36gFeCerndimjO0C2oagYNmq0NlUv4lTamng7e29GlRTGIIYNLMVV-l6BU_pAyHxgbi-evxixk_2KUtG530UASs1kwiv4Rh_d6fnwmggIUfXCzCwcv1vxhaIWVLRnIPM5cQA0mkdcqjcid_D-KzAsP9pGsqh9u2JViDrAnj2aXfLiYGj7XVGhg.blQv3wklhGlqUeWlj2_1Z03i7PG_JX8J9u94NjVHQYE&dib_tag=se&keywords=silikonschlauch%2B5mm&qid=1772531638&sr=8-3-spons&aref=YRg9eceQvl&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&th=1) |
| Hydraulic connectors | ID: 8mm (same as tube); thread 1/8” | 4 | [https://www.amazon.de/Stück-Steckverschraubung-Schnellsteckverbinder-Push-8mm/dp/B0108HHGLK?th=1](https://www.amazon.de/St%C3%BCck-Steckverschraubung-Schnellsteckverbinder-Push-8mm/dp/B0108HHGLK?th=1) |
| Female XT-90 connectors | optional, but easier than clamping power to the pumps | 2 |  |
| Plastic box to store, potentially foam | IKEA Samla (39x28x14cm) works perfectly | 1 | https://www.ikea.com/de/de/p/samla-box-mit-deckel-transparent-s69440836/ |
| Watertight container for the membrane |  | 1 |  |
| (Adhesive) foam and small rubber feet | Foam: 1-2mm thick  (adhesion not required, but easier to assemble) | rubber feet: 4-6 pcs. |  |
| Teflon tape |  |  |  |

 

# 4. Manufacturing the cell

## 3D printing:

### **Material selection and compatibility testing:**

Running the cell with the two electrolytes specified above, both PLA and PETG were identified as suitable polymers, as the electrolytes used are relatively pH-neutral compared to the electrolytes used in industrial-grade systems (e.g. Vanadium), reducing the necessity for more chemically resistant materials. However, should the cell be supposed to be used primarily with other electrolytes, it is strongly recommend to test the chemical compatibility with the polymers beforehand. The easiest testing method is to print a cylinder with a closed bottom and consistent wall thickness of around 0,8mm and filling it with the preferred electrolyte for a minimum of 24 hours. Leakage or a loss of weight of the printed part (to be measured before and after it has been subjected to the electrolyte and has fully dried again using a precision scale) indicates the polymer to be unsuitable in the long term. The cylinders wall thickness of around 0.8mm closely mimics the flow-frame’s minimal wall thickness of just 0.5mm, while ensuring enough stability. Such a testing cylinder can be found in the file directory.

### Print Instructions:

*Note: All print instructions below are for FDM printers, as we never had the possibility to use SLA/SLS-printers. That being said, using a SLA-printer for this application might bring in even better results, considering its supreme accuracy and better handling of unsupported overhangs.*

1. Pump Casing:
    
    The pump casing should be printed in its original orientation. There are no supports necessary, although some post-processing with a small file or a Dremel might be required for the overhangs of the vertically oriented holes, depending on the amount of sagging produced by the 3D-Printer.
    
2. Cell:
    
    Regardless of the process/file used (see below), the following settings are a recommended minimum/maximum:
    
    - Layer height of max. 0.15mm (relevant for thread quality)
    - Min. 3 vertical perimeters (”walls”) and 25% infill → possibly varying dependent on the achieved water-tightness of the print
    - For the use of supports, see below.
    

The pump casing can be printed with a material and print settings of choice, as neither strength nor chemical compatibility are major concerns here. 

The printing of the cell (also referred to as “flow-frame”) is vastly more complicated, both in the process itself and in the requirements for the 3D-Printer used. The need for a fully waterproof cell, threads, large overhangs within the inlet manifolds, and a minimal printing size of just 1mm² on the X-Y-plane and 0.5mm vertically (Z-plane) require a well-maintained and precise 3D-printer. It should be noted that, especially for the inlet manifolds, sagging of the layers above and extreme stringing can easily clog the individual channels, greatly restricting the flow of electrolytes and thereby reducing the cell’s performance.
In the center of the flow-frame is a square 40x40mm cavity, which will most likely require the use of supports, as its top cover is relatively thick and therefore heavy. There are two options for printing the cell:

1. Firstly, should you be confident in your printer’s auto-generated supports and don’t mind removing them, you can print the “Cell_V4_mono_…” files and use auto-generated supports for the centre cavity. In this case, make sure that none of the auto-generated supports reach into the inlet manifolds, as it’s pillars should provide enough support themselves, and foreign supports are nearly impossible to remove without damaging the thin base plate.
2. Secondly, should you want to avoid using auto-generated supports, you can print the “Cell_V4_interior” and “Cell_V4_exterior_…” files. In this case, the “interior” part is a simple rectangular plate topping the cavity, which is printed beforehand and is inserted into the cell afterwards during the print, thereby functioning as a support for the following layers. Start by printing the “Cell_V4_interior” part. I would recommend printing the part twice to begin with, as the part is identical in both of the flow frames and is therefore needed twice. When slicing the “Cell_V4_exterior” part, add a print pause just before the first layer covering the cavity is to be printed (height around 12,9mm). Once the print pauses, simply insert the plate into the slot around the cavity. 
    
    
    ![image.png](attachment:a5004e2b-e4cb-40ec-978a-572256bffdb7:image.png)
    
    ![image.png](attachment:cde8bee5-4e18-4fa6-b95a-0ea0c751f0cb:image.png)
    
    Please note that the plate is not symmetric but requires a specific orientation because of two threaded holes, whose orientation needs to match the orientation of the holes in the rest of the print (see pictures below). It is important to make sure that the slab lies fully flat in the recess and does not stick out, as the extruder nozzle could otherwise catch the plate, or all following layers could potentially shift. If you have access to a suitable glue (e.g. superglue or glue made specifically for bonding 3D-prints), it is only beneficial to glue the plate in place, as it lowers both the risk of the plate shifting, as well as the risk of fluids leaking out of the chamber, should a layer fault occur on the first layer printed after the pause (either from the plate rising up or from the part having cooled down too much).
    
    ![Bildschirmfoto 2026-03-05 um 10.17.50.png](attachment:a7036536-0e6d-416c-8d02-a40b9b3ec91a:Bildschirmfoto_2026-03-05_um_10.17.50.png)
    
    ![Bildschirmfoto 2026-03-05 um 10.17.31.png](attachment:c798c5de-4a17-4de7-8e4f-10f76980d2b6:Bildschirmfoto_2026-03-05_um_10.17.31.png)
    

In both cases, there is an “…A” and “…B” file, which both need to be printed. The only difference between them lies in the letter marked on them - it is, however, strongly recommended to print both of them (and not one two times), as the instructions are vastly easier to follow when the flow-frames are clearly identifiable.

Post-processing of the printed flow-frames is not necessary in general, except for the removal of any unwanted material (both shifted/sagged down or from stringing) from the chamber itself and from the inlet manifolds. Depending on the print’s quality, recutting the two central M5 threads on each flow frame might be required additionally. The standard way of doing so would be to use a respective M5 thread cutter. Should a thread cutter not be available, it is possible to very (!!) carefully and slowly cut the threads using an M5 bolt, at least when printing the cell from PLA. Carefully twist the bolt back and forth every few revolutions to ensure cutting the chips of material, and remove the bolt every dozen revolutions to clean both the parts and the bolt’s threads from any buildup material.

## Part Assembly:

### Assembly of the flow frames:

The printed and possibly post-processed flow frames need to be fit with hydraulic quick-connectors, which will connect the silicon tubes used for the electrolytes to the manifolds. These connectors screw into the two large threads, one on each side, of the flow frames and can be mounted by using a 14mm wrench and need to be tightened until their seals sit flush with the 3D-printed surface. Whether these connectors can be screwed in or require pre-cut threads is again dependent on the print quality. Should manually re-cut threads be required, this can be done by either using a thread cutter as well - be aware that these threads are not metric but 1/8" x 8mm - or by using the connectors themselves as improvised thread cutters. Carefully twist the connectors back and forth every few revolutions to ensure cutting the chips of material, and remove the bolt every dozen revolutions to clean both the parts and the connectors’ threads from any buildup material.

### Assembly of the pump casings:

**Dampening (optional, but strongly recommended):**

The pumps used in this project and specified above are comparatively cheap, but come with the downside of being very badly balanced, causing terrible noise and vibrations, at least for something of their size. For this reason, I would strongly recommend padding the pump casing. This can be done in several ways:
The pump has contact with the casing on three surfaces in total: the one it is bolted to and two horizontal supports. Cut pieces from an (ideally adhesive) foam approximately one millimeter thick and apply them to the contact surfaces. A 3D-printable template for the shape of the foam required for the pump’s main contact surface can be found in the files directory. In case of the horizontal surfaces, a one millimeter offset is already accounted for in the model. Alternatively/Additionally, small rubber feet can be applied to the casing’s bottom.

 

**Assembly:**

The pump is simply inserted into the casing with the motor side first and is bolted to the casing using the four countersunk screws specified above (the process is tedious, thanks to the pump's design). To simplify the connection of power cables to the pump, a regular female XT-90-Connector can be soldered to the pump's terminals, which enables the use of “banana-plug” cables. Otherwise, the cables can simply be attached to the terminals by standard “alligator clamps”.

## Preparation of additional parts:

**Copper Plates:**

Cut two square copper plates, one for each of the flow frames, each with a lateral length of just slightly below 40mm to fit into the flow frames’ centre chamber. Accuracy is not a major concern in this case. The plates should fit tightly, but not get stuck inside the chambers or be overly hard to remove. It should, however, be noted that a greater accuracy does reduce the amount of electrolyte that flows behind the copper plates and therefore greatly reduces the risk of the cell leaking.

**Graphite Plates:**

Cut two square graphite plates, one for each of the flow frames, with the same length and tolerance specified for the copper plates above.

**Membrane:**

The membrane needs to be cut to the required dimensions. The minimum size of the membrane is determined by the outside diameter of the rubber gaskets used, e.g. in case of the ones linked in the parts list, 78mm. This is necessary in order to make sure that a sufficient seal can be created between the membrane and gasket, which is greatly restricted when the contact area between gasket and membrane is not large enough. Instead cut the membrane in a way that guarantees that all of the gasket’s area is covered.

The Nafion N-117 membrane is supplied in a dry state by the manufacturer. However, once the membrane has had contact with fluid, it can never be allowed to dry again, as it will crack and be rendered entirely unusable. It therefore has to be stored submerged in liquid permanently. Either after the first contact with fluid (in most cases after the first run) or before, prepare a large enough sealable container by filling it with distilled (!) ****water and dissolving a few grams of ammonium sulfate (conducting salt). Always make sure that the membrane is stored correctly after every run and that it is fully submerged in the fluid. Do not store under extreme heat or in direct sunlight.

**Silicon Tubes:**

The cell requires a total of six silicon tubes to cycle the electrolytes throughout all components. The length of the tubes can be varied based on the overall length of the tubes available. Two of the tubes should be slightly longer, with the remaining four tubes having the same length. Based on our tests, the following measurements are suitable minimum lengths:

- 2x 600mm
- 4x 450mm

Generally speaking, longer tubes provide more flexibility and space when working with the cell, facilitating user friendliness. 

## Preparing the pump for Electrolytes:

Take one of the four shorter silicon tubes and place one of its ends on one of the pump's four outputs. Firmly slip the end over the cone-shaped output until it fits securely - the tube’s ends should sit roughly one centimeter down on the cone. If possible, use a zip tie to further secure the connection.
Repeat the process with the three tubes remaining.

# 5. Setup of the Cell

## Preparation of Electrolytes:

A redox flow cell consists of two different electrolytes — a posolyte and a negolyte. Both must first be prepared. 

Wearing personal protection equipment (lab coat, disposable gloves, and safety goggles) is strongly recommended for the following steps (based on personal “experiences”).

**Preparation of the posolyte:**

1. Measure out 100 ml of distilled water using the measuring cylinder.
2. First, weigh out 3 g of ammonium sulfate (conducting salt) and then 9.68g of potassium hexacyanoferrat using the precision scale.
3. Pour the distilled water, the ammonium sulfate, and the potassium hexacyanoferrate into a sealable round-bottom flask and shake the flask until a homogeneous solution is obtained.

**Preparation of the negolyte:**

1. Measure out 50 ml of distilled water using the measuring cylinder.
2. Using the precision scale, first weigh out 1.74 g of ammonium sulfate (conducting salt) and then 4.22 g of 2,7-anthraquinone
disulfonic acid.
3. Add the distilled water, the ammonium sulfate, and the 2,7-anthraquinone disulfonic acid to a sealable round-bottom flask and shake the flask until a homogeneous solution is obtained.

**Determining the negative and positive flow-frame:**

The decision which side of the cell will serve as anode and which as cathode depends on the filling of the cell with electrolyte, more specifically on which electrolyte - the negolyte or the posolyte - is connected to which flow frame. The electric circuit is created according to this decision.

1. It is strongly recommended to label the beakers (with a marker): One beaker is to be labeled “A”, the other one “B”. This creates a continuous system, in which each part cycling electrolyte, including the 3D-printed ones, is labeled “A” or “B” correspondingly, allowing for easier and less error-prone operation.
2. Simply fill one beaker with one of the electrolytes and the other one with the other electrolyte. Remember which electrolyte has been filled into which beaker. This is aided by the clearly different colors.

## Additional preparations:

The graphite fleece is the only other part, except the electrolytes, that is single-use and needs to be prepared again for each run. Cut two square pieces measuring precisely 40x40mm (as precisely as possible with a scalpel or small scissors) from the fleece. These pieces can also be prepared in large quantities beforehand to reduce the setup time required for each run.

## Assembly of the main cell:

1. Lie both flow-frames on their backs, with the flat plane facing towards you. The rectangular recess in the centre of the flow-frame should be clearly visible. First, put a copper plate in each recess, followed by a graphite plate, and push down firmly. There should be two plates in each frame, with the upper edge of the graphite plate lining up so that the inlet manifolds to each side of the recess are fully visible. If that is not the case, try pressing down more firmly or check if the plates have been cut too large to fit flush into the recess. Afterwards, press a piece of graphite fleece into each recess.
2. Take one of the flow frames. Press the four long hex bolts through the four symmetrically arranged screw holes of the flow frame so that the ends are on the inside (flat plane). The parts tolerance should allow for the screws’ hexagonal heads to fit into a specific recess on the outside by simply pressing them in, preventing the bolt from rotating. An alternative method of assembly is specified below.
3. Concerning the flow-frame now containing the bolts: Center one of the rubber gaskets around the central recess and make sure that it lies as centered as possible. Lay the membrane on top and center it as well, making sure that all the gasket's surface area is covered by the membrane. Stack another gasket on top.
4. Take the other flow-frame and turn it over, the outside facing you. It might be necessary to cover the recess with a finger, as the plates could fall out otherwise. Carefully align the flow-frames’ screw holes with the other frames’ bolts and push it down, making sure that the frames make contact evenly to prevent the gaskets from becoming misaligned. The gaskets and membranes’ alignment is critical to achieve a seal - should their alignment be possibly compromised, repeat steps three and four until successful. Then put a washer and nut onto each bolt and tighten the nuts - at first by hand, then with the 8mm wrench - until the flow-frames slightly (!) curve inwards under the force.
    
    **Alternative method:**
    
    Alternatively, it is also possible to skip step two, instead starting with step three and aligning the cells manually, and only pushing through the bolts after aligning. The process of tightening them stays the same. From experience, both methods have been equally capable and are only based on personal preference. 
    
5. Finally, screw in the remaining four shorter bolts into the two threaded holes in the centre of each flow-frame. These will serve as current collectors once the cell is running. Tighten until there is a noticeable increase in resistance from the bolts, caused by contact with the copper plates. Alternatively, it is also possible to determine when the bolts are tightened enough by comparing the overall length of the bolt to the length of the still visible part of the bolt minus the length of the threaded hole: The bolt is tightened enough, when the bolts overall length minus the threaded holes length (fixed at 10mm) are equal to the length of what is still visible from the bolt.

## Connecting the electrolyte circuit and electrical circuit:

### Electrolyte Circuit:

1. The pump consists of two labeled pump-heads, each equipped with two silicon tubes. Take the end of one of the tubes from the pump head which is labeled “A” and place it in the beaker marked “A”.  Place one end of a longer silicon tube (not attached to the pump) in the same beaker and connect the other end to one of the hydraulic connectors on the flow-frame labeled “A”. Lastly, connect the remaining tube from pump-head “A” to the remaining connector on side “A” of the flow-frame.
2. Take the end of one of the tubes from the pump head which is labeled “B” and place it in the beaker marked “B”.  Place one end of a longer silicon tube (not attached to the pump) in the same beaker and connect the other end to one of the hydraulic connectors on the flow-frame labeled “B”. Lastly, connect the remaining tube from pump-head “B” to the remaining connector on side “B” of the flow-frame.

### Electrical circuit:

1. Connect the PSU to the pump while considering the polarity of the terminals. As long as all ends of the tubes in both beakers are fully submerged in the electrolyte to prevent the pumps from running dry, the polarity and its resulting direction of rotation are not of major relevance.
2. Add crocodile clips to all four hex bolts from cell-assembly step five.
3. Connect a cable from the negative terminal of either the same PSU’s second set of outputs or of a different PSU (see “Electrical Equipment”) to the negative terminal of whatever device is being used as a amperemeter. 
4. At this point, the polarity of the electrolytes becomes relevant. From the amperemeter's positive terminal, connect a cable to one of the two current collectors (central bolts) on the flow-frame’s side that is filled/connected to the negolyte (anthraquinone). Depending on the fill of the beakers, this can be either side “A” or “B”. From the same side’s second current collector, connect a cable to the positive terminal of the device functioning as a voltmeter.
5. From the negative terminal of the voltmeter, connect a cable to the current collector of the flow-frame's side that runs the posolyte (potassium hexacyanoferrate). This side is never (!) the one to which cables are already attached or which is connected to the reddish anthraquinone. From this side’s remaining unoccupied current collector - which should be the only one that has no electrical connections yet - connect the last cable to the PSUs positive terminal.
6. Confirmation: Firstly, make sure that the set of outputs the pump’s energy supply is connected to is not the same as the one to which the cell or any of the measuring equipment is connected. Secondly, make sure that the crocodile clips attached to the current collectors do not touch, which would result in shorting the cell and measuring equipment otherwise. Adding an insulating layer between close clips is already sufficient.
7. Power on the multimeters (or other measuring devices) and select the range. For the voltmeter, V, and for the amperemeter, mA, should be sufficient.  

A more easily understandable graphical representation of the entire circuit looks as follows:

![Bildschirmfoto 2026-03-04 um 00.20.59.png](attachment:cf55abd4-7f84-4664-b538-bf28f3cc87b7:Bildschirmfoto_2026-03-04_um_00.20.59.png)

*Note that in the graphic, the two pump-heads appear as two separated devices to allow for a clearer depiction. In reality, both are part of the same device, share the same motor, and are therefore connected by the same power cables/terminals, not two separate ones.* 

# 6. Operating the Cell

## Charging:

After the previous instructions have been completed and the cell has been assembled correctly, the actual run can start.

1. Start the pumps and increase the voltage until the pumps slowly but steadily cycle electrolyte. With the setup the cell has been operated with previously, such speed corresponded to roughly four volts - this is however dependent on the pump used, the power supply, the resistance in cables, etc. Check for any leaks or other problems. If that is not the case, progress to step two.
2. Slowly increase the pump speed to operating level, at which the flow rate should be high enough to have the electrolytes cycling throughout the system smoothly/uninterrupted at a medium speed. A major problem lies in the lack of comparability of pump speed. In general, the pumps need to be far from running under full load in order to fulfill their purpose, as it is usually enough to have the electrolytes cycling throughout the system smoothly at medium speed. In case of our own experiments, this corresponded to a voltage within 8-10 volts; however even we did experience large fluctuations, based on different levels of electrical resistance varying between newer and older cables. In conclusion, voltage specifications are fragile and need to be approached cautiously. At the time of writing, we never did conduct tests to determine the actual flow rate required (in Volume/milliliters), resulting in this core value being missing.  
3. Next, start charging the cell by activating the second output/power supply connected directly to the cell. It is always recommended to read the values mentioned from the multimeters, rather than the power supply’s own display of voltage/current, should it provide such data in the first place. Always have caution when increasing power, as our experiments have shown that certain power supplies can be very sensitive, possibly triggering power spikes, which will most definitely burn the membrane - something that has occurred previously. 
The cell has to be charged at a current of 0.8 ampere, until the voltage inside the cell (reading of the voltmeter) reaches 1.1 volts.
4. After a short period of time, the electrolytes will begin to change their color. The dark-red anthraquinone disulfone (negolyte) will brighten and become yellow-orange, while the previously yellow potassium hexaferricyanide (posolyte) darkens to become orange. In conclusions, the charging-process roughly swaps the electrolytes colors. After about two minutes, the cell should have reached its peak voltage of - as for now - 1.1 volts.

## Discharging:

The process of discharging the cell involves exchanging the power supply used for charging the cell for an electronic load. The most suitable method uses an (artificial) electronic load rather than a more standard consumer such as a motor or LED, as it offers smaller increments for selecting energy consumption and an overall more accurate and stable energy discharge, facilitating more repeatable testing. That being said, for applications focused more on experimenting than on accurate testing, integrating a more practical use for the cell’s stored energy such as a small car, robot or lamp could improve the cells attractiveness for these use cases. Additionally, likewise alternatives would positively impact the cells overall cost, as they are cheaper than most laboratory-grade electronic loads.

1. To discharge the cell, the two charging cables connected to the cell at the power supply are removed. Afterwards, the cables can be connected to the positive/negative terminals of a consumer, preferably an electronic load (see above).
2. The energy being drawn from the cell should be lower than or equal two the maximum charging power of 1.1 volts and 0.8 ampere. Depending on the consumer used, the energy consumption can either be toggled directly (electrical load or comparable) or needs to be controlled using resistors.  

# 7. Disassembly

**Flushing the system:**

Before the cell can be disassembled, all the electrolyte has to be cleared out. First, the tube endings in both beakers are pulled out slightly until they are above the waterline, preventing further electrolytes from entering the system. The pumps can now be run on low speed until all electrolyte has been pumped out of the cell and no further fluid is running from the tubes. Next, the electrolyte-beakers can be exchanged with an unused beaker filled with ca. 150ml of distilled water, and all tube endings are placed inside. The pumps are run again, until the electrolyte seems to have been flushed out of the cell completely. It might be necessary to repeat this process a further 1-3 times. 

**Electric circuit:**

The entire electric circuit can be completely disassembled. For reasons of safety, the power should be cut first, followed by powering down and disconnecting the multimeters to prevent them from accidental short-circuits.

**Disassembly of the cell:**

1. Disconnect all silicon tubes connected to the cell.
2. To facilitate the cells’ handling while it is being disassembled, first remove the four current-collector-bolts (two on each side).
3. Undo the hex bolts clamping the cell together and remove them entirely.
4. Protecting the delicate membrane is a key objective during disassembly. Take out the membrane first, before resuming with anything else, and rinse it with distilled water to remove any visible contamination with electrolyte. Then place it into its designated container, making sure that it is fully submerged in fluid and not subjected to direct sunlight while in storage. 
5. Remove and dispose of the graphite fleece.

**Cleaning:**

1. Following these steps, all remaining components (flow-frames, tubes, plates, bolts, gaskets) can be cleaned. As these parts are not sensitive, cleaning them under flowing water with a brush and regular dish soap is entirely possible. The tubes should only be rinsed out with water. Make sure to especially clean the cells threads and inlet manifolds inside the central cavity, as they are the main distributors of the electrolyte and are hard to reach, facilitating the buildup of electrolyte residue. 
2. Dry all parts immediately - especially but not limited to the bolts and copper/graphite plates - as these can corrode very quickly (at least on the surface).
3. Finally, wipe the flow-frames and plates with a paper towel and cleaning alcohol (see the list of required chemicals above for suitable examples) to remove any contamination, visible or not, that could negatively impact the cell’s performance.

# 8. Bug fixes and common problems

1. **The plates are stuck within the flow frames:** 
    
    Take one or ideally two thin cylindrical objects (e.g. the back of thin pencils or a paintbrush) and insert them into the two central threaded holes of the current collectors from the outside and push down simultaneously or in small increments one by one. The plates should drop out.  Should this issue occur more often, consider filing down the plates slightly, as removing them forcefully too often will inevitably damage the cell’s thin base plate. 
    
2. **The current collectors leak fluid:**
    
    The current collectors are arguably one of the cell’s weak spots regarding potential leakage as the threads are the only barrier keeping the system sealed. As they get worn down over time, especially since they are only made out of plastic, fluid can slowly channel up through the threads. Solving this issue involves wrapping one to two layers of Teflon tape around the bolts before screwing them in. The Teflon tape further seals the gap while not restricting the bolts as much as preventing them from fitting.
    
3. **The membrane/gaskets leak(s) fluid:**
    
    Check if the bolts clamping the two flow frames are tightend enough or if further tightening potentially solves the problem. Otherwise, the rubber gaskets might have to be replaced, as they are wearing parts as well and will deform over time. Should different gaskets then the ones specified above have been used, they might have other properties regarding hardness etc. and therefore be less suitable for this specific use case. In our experience, the process of finding suitable gaskets has been the most extensive and faulty process of the entire project.
    
4. **The electrical circuit does not work properly or values do not make sense:** 
    
    Possibly, this might not be a common problem, but it is a problem we faced ourselves. If the pumps suddenly do not work with the same power previously applied and the cell does not charge properly compared to previous runs, selecting different cables could make a difference, at least if different ones might have been used previously. Especially in the setting of a high school, where numerous and possibly not well maintained cable are available, some of them might have defects such as a faulty resistance due to corrosion or similar. In our test run, this caused the entire system to not work properly, which was fixed entirely by switching to newer cables. Not a common problem, but one that is not obvious should it occur.
    

# 9. Media Pool

A collection of various images and videos of the cell and it’s assembly can be found in the media file-tree.

# 10. Conclusion

We would like to express our sincere thanks to everyone at our high school who supported us in our research and made the entire “jugend forscht” project possible in the first place - most notably Mrs. Grunewald. We would also like to thank the Technical University (TU) Clausthal-Zellerfeld and Mr. Söffker for their ongoing support and technical expertise. 

© This documentation was written by Jonathan Danner in March 2026.
© 2026 Jonathan Danner, Hams Alek, and Manuel Berkenhagen. All rights reserved. Copyright is retained by the authors.
