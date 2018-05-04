---
layout: default
title:  Tutorials
permalink: /tutorials/
---

<style>
.menutitle {
    display: inline-block;
}

.tab {
	padding-left:5em;
}

details[open] summary ~ * {
  animation: sweep .5s ease-in-out;
}

@keyframes sweep {
  0%    {opacity: 0; margin-left: -10px}
  100%  {opacity: 1; margin-left: 0px}
}

</style>

<h1> Getting started </h1>

<details>
<summary><h2 class="menutitle"> Introduction</h2></summary>

<p class="retrait"> MyDEP is a Java based standalone software which allows to study dielectric particle response to AC electric fields and to analyse the electric properties of biological cells.
It consists of a Graphical User Interface (GUI) supporting a literature-based database. This tool can also be used with the user's own data sets. </p>

<h2 class="menutitle"> Installation and system requirements </h2>

<p> MyDEP can be run on Windows, Mac OS X or Linux/Ubuntu operating systems. It requires Java to be installed on your system.</p>
<p> Download the latest version of MyDEP by clicking on the "Free Download" button in the page header.
Unzip the folder (zip archive) and open it. Double-click on the mydep.jar file.</p>
<p> For OS X users, depending on the security preferences, the following message might be displayed: </p>

<div class="DIVimage60">
    <img class="im" src='/assets/img/image01_mac.png' />
</div>
<p>In this case click on OK, go to System Preferences -> Security and Privacy. Under the General tab the following info should appear:</p>

<div class="DIVimage60">
    <img class="im" src='/assets/img/image02_mac.png' />
</div>

<p> Click on "Open anyway" -> Open </p>

<div class="DIVimage60">
    <img class="im" src='/assets/img/image03_mac.png' />
</div>

<p> The "mydep.ini" file will be created containing all your preferences and the following screen will appear with the application: </p>

<div class="DIVimage">
    <img class="im" src='/assets/img/image04_MyDEP.png' />
</div>

 </details>
<details>
<summary><h2 class="menutitle"> User interface structure </h2></summary>

<div class="DIVimage">
    <img class="im" src='/assets/img/Image05_MyDEP_cadreRouge_number_menubar.png' />
</div>

<p> The interface is constituted of nine different parts: </p>
<ol>
  <li> Medium </li>
  <li> Frequencies </li>
  <li> Model </li>
  <li> Sweep </li>
  <li> Calculate </li>
  <li> Graphs </li>
  <li> Results </li>
  <li> Display options </li>
  <li> Menu bar </li>
</ol>  

The following section describes them one by one.

It should be noted that tooltips are available for most of the interface parameters. To access them, the user should place the mouse cursor on the desired parameter.

  <details><summary class="tab"><h4 class="menutitle"> 1. Medium </h4> </summary><p class="retrait"> In this section, the user can choose the dielectric properties of the medium which are $\sigma_m$, the electrical conductivity and $\epsilon_m$, the relative permittivity.
	An additional box allows to indicate the value of the volume fraction $\Phi$. It corresponds to the fraction of the volume of the cells compared to the volume of liquid. This value is needed only for the calculation of the permittivity and conductivity of the suspension of particles with the Maxwell and Asami methods that will be described later.</p>
  </details>
  <details><summary class="tab"><h4 class="menutitle"> 2. Frequencies </h4></summary> <p> In this section, the user can choose the start and stop frequencies of the graph as well as the number of points, logarithmically spaced, that will be used. </p>
</details>
  <details><summary class="tab"><h4 class="menutitle"> 3. Model </h4></summary> <p> In this section, the user can choose the particle model that will be implemented. Dielectric particles such as cells are usually represented as concentric shells. Here the user can specify the number of layers that will be used. Moreover, the particle shape can be either spherical or ellipsoidal. The possible models are: </p>

  <ul>
      <li> <b>Homogeneous particle:</b> this model corresponds to a completely homogeneous particle.
        <br><br>
        <div class="DIVimage">
            <img class="im" src='/assets/img/image06_homogeneous.png' />
        </div><br>
      </li>
      <li> <b>Single-shell:</b> this model corresponds to a particle with an outside layer. For a cell it typically represents a cytoplasm surrounded by a lipid membrane.
        <br><br>
        <div class="DIVimage">
            <img class="im" src='/assets/img/image07_single.png' />
        </div><br>
      </li>
      <li> <b>Two-shell:</b> this model corresponds to a particle with two outside layers. For a cell it corresponds to a cytoplasm surrounded by a cell membrane and a cell wall.
        <br><br>
        <div class="DIVimage">
            <img class="im" src='/assets/img/image08_two.png' />
        </div><br>
      </li>
      <li> <b>Three-shell:</b> this model corresponds to a cell with one outside layer and a nucleus occupying a significant volume. The order of the layers from the inside to the outside is nucleoplasm, nuclear envelope, cytoplasm and cell membrane.
        <br><br>
        <div class="DIVimage">
            <img class="im" src='/assets/img/image09_three.png' />
        </div><br>
      </li>
      <li> <b>Four-shell:</b> this model corresponds to a cell with two outside layers and a nucleus occupying a significant volume. The order of the layers from the inside to the outside is nucleoplasm, nuclear envelope, cytoplasm, cell membrane and cell wall.
        <br><br>
        <div class="DIVimage">
            <img class="im" src='/assets/img/image10_four.png' />
        </div><br>
      </li>
  </ul>  

  <p>Here is a summarized description of the implemented cell models (the four-shell model is not represented here):</p>
  <div>
      <img class="im" src='/assets/img/image11_CellModel.png' />
  </div>

  </details>
  <details><summary class="tab"><h4 class="menutitle"> 4. Sweep </h4></summary> <p class="retrait"> The Sweep button, once pressed, performs a sweep on different values of the selected parameter. To change the parameter on which the sweep is performed, click on the Sweep parameter and select the desired parameter (cf following image). The number of points used, as well as the min and max value, can also be specified. If the log button is pressed, the values will be logarithmically distributed (linearly distributed otherwise). </p>
  <div class="DIVimage60">
      <img class="im" src='/assets/img/image12_SweepParameters.png' />
  </div>

  </details>
  <details><summary class="tab"><h4 class="menutitle"> 5. Calculate </h4></summary> <p class="retrait"> The Calculate button performs the corresponding calculation displayed in the Graphs section. The orange color of the button indicates that no calculation has been performed. The button turns green once the calculation is done.</p>
	<p class="retrait">If the Sweep button is pressed, the progression of the calculation will be displayed on this button by using a progress bar.</p>

  </details>
  <details><summary class="tab"><h4 class="menutitle"> 6. Graphs </h4></summary> <p class="retrait"> The graphs displayed in this section are the following:</p>
	<ul>
    <li> Clausius-Mossotti factor, abbreviated CM factor (real and/or imaginary part).</li>
    <li> Permittivity:
        <ul>
          <li> $\varepsilon_{eq}Particle$: the equivalent relative permittivity of the particle. </li>
          <li> $\varepsilon_{eq}Mixture$: the equivalent relative permittivity of the particles in suspension in the medium at the given volume fraction.</li>
        </ul>  
    </li>    
    <li> Conductivity:
        <ul>
          <li> $\sigma_{eq}Particle$: the equivalent electrical conductivity of the particle. </li>
          <li> $\sigma_{eq}Mixture$: the equivalent electrical conductivity of the particles in suspension in the medium at the given volume fraction.</li>
        </ul>  
    </li>
    <li>Crossover: This graph corresponds to the different crossover frequencies when the sweep mode is used.
    </li>
  </ul>

  <p> <b>Editing curves:</b></p>
  <ul>
      <li> <b>Zooming </b>:<br> You can zoom the graph using the scroll-wheel of your mouse or the zoom functionality of your trackpad. </li>
      <li> <b>Curve properties: </b><br>
      A left click on a displayed curve will select the curve which will appear in a thicker linestyle. The corresponding parameters used for its creation will be displayed in the left part of the interface (Medium/Frequencies/Model).<br>
      A right click on a displayed curve will cause a popup menu to appear with the following options:
      <ul>
        <li>Curve parameters: The line style of the curve and its width can be adjusted as well as its color with Swatches, HSV, HSL, RGB and CMYK color models.</li>
        <li> Sweep curve parameters:
         If the curve was generated in the sweep mode (sweep of one parameter), this menu enables to modify the line style, line width and color of all the curves generated during the sweep. </li>
        <li> Delete curve: Delete the specific curve. </li>
      </ul>
      </li>

      <li> <b>Legend:</b><br>
      The legend can be moved in the graph by dragging it. The following parameters can be modified by right-clicking on the legend -> Legend parameters:
      <ul>
      <li> Opacity of the legend: By default, the legend background is opaque but can become transparent by unclicking the button.</li>
      <li> Anchoring (horizontal and vertical): This corresponds to the fixed point when the MyDEP interface size is modified on screen or printed. </li>
      <li> Font and font size </li>
      <li> Font color and background color</li>
      </ul><br>
      <div class="DIVimage">
          <img class="im" src='/assets/img/image13_LegendParameters.png' />
      </div>
      <br>
      In the Sweep mode the legend will display the properties of the last generated curve (default mode) or the selected curve.
      </li>

      <li> <b>Axis properties:</b><br>
      A right click on the axes will give access to the Grid and labels parameters menu. This menu offers the possibility to change:

      <ul>
      <li> The displayed axis properties: horizontal and vertical axis labels (possibility to use html for special characters), the font and the font size</li>
      <li> The unit properties: font and font size. </li>
      <li> Font and font size. </li>
      <li> The major grid and minor grid parameters: line style, line width and color.</li>
      </ul><br>
      <div class="DIVimage">
          <img class="im" src='/assets/img/image14_GridProperties.png' />
      </div>
      <br>
      </li>
</ul>
     </details>
  <details><summary class="tab"><h4 class="menutitle"> 7. Results </h4> </summary><p class="retrait"> This section corresponds to an analysis of part of the graphs. The part is different depending on the selected graph:</p>
      <ul>
        <li>CM factor tab :
          <ul>
          <li> $Re[CM(f)]$ and $Im[CM(f)]$ button: if pressed the corresponding curves will be displayed.</li>
          <li> Min Max auto button: if pressed the Min and Max value will be adjusted automatically. Otherwise they will correspond to yAxis_min and yAxis_max.</li>
          <li> 	Fcursor button: a vertical line will be displayed at the frequency written in the box, whose unit can be adjusted (Hz, KHz, MHz or GHz). The value can also be adjusted with the corresponding slider. The values of $Re[CM(f)]$, $Im[CM(f)]$, $F_{DEP}/\nabla E^2_{RMS}$ and $\Gamma_{ROT}/|E^2| $.</li>
          <li> Baseline button: a horizontal line will be displayed at the value written in the box. The value can also be adjusted with the corresponding slider.</li>
          <li>Legend button: A click on the Legend button will open a popup menu where the properties to display will be available by ticking the corresponding tickbox. The order of the displayed parameters can be modified by clicking on the corresponding arrows. The "user text" box can be used to display the desired text, using html language when needed.</li>
          <li>Crossover frequencies: the different crossover frequencies correspond to the frequencies at which $Re(CM) = 0$</li>
          </ul>
        </li>
        <li> Permittivity and Conductivity tabs:
          <ul>
            <li> Particle and Mixture buttons: if pressed the corresponding curves will be displayed </li>
            <li> 	Min Max auto button: if pressed the Min and Max value will be adjusted automatically. Otherwise, they will be correspond to $\varepsilon_{min}$ and $\varepsilon_{max}$ (respectively $\sigma_{min}$ and $\sigma_{max}$).</li>
            <li>	Fcursor: a vertical line will be displayed at the frequency written in the box, whose unit can be adjusted (Hz, KHz, MHz or GHz). The value can also be adjusted with the corresponding slider. The values of $\varepsilon_{eq}Particle$ and $\varepsilon_{eq}Mixture$  (respectively $\sigma_{eq}Particle$ and $\sigma_{eq}Mixture$).</li>
            <li> All the other buttons have similar behavior as described in the CM factor tab.</li>
          </ul>
        </li>    
      <li>	Crossover tab </li>
      </ul>


     </details>
<details><summary class="tab"><h4 class="menutitle"> 8. Display options </h4></summary>
      <p> This section contains different buttons to adjust the properties of the graphs displayed in the Graphs section:</p>
      <ul>

      	 <li>Clear fig button: Clear fig removes all curves from the Graph section</li>
         <li> X Log button: If X Log is pressed the x axis will be displayed with a logarithmic scale, otherwise with a linear scale.</li>
         <li> Y Log button: If Y Log is pressed the x axis will be displayed with a logarithmic scale, otherwise with a linear scale.</li>
         <li> Hold on button:  Hold on retains plots in the current axes so that new plots added to the axes do not delete existing plots.</li>
         <li> Reset zoom button: Reset zoom resets the graph to its initial zoom.</li>
         <li>Legend button: Legend displays the legend in the graph.</li>
      </ul>

      </details>
  <details><summary class="tab"><h4 class="menutitle"> 9. Menu bar </h4></summary> <p>The menu bar contains different categories:</p>
      <ul>
        <li>File
        <ul><li>Quit: Quit the interface.</li></ul></li>
        <li> Data
        <ul><li>Import: Import a new database.</li>
            <li>Export:
              <ul> <li> user database: Export the user database (user_database.txt) at the desired location. By default the user_database.txt file is generated in the mydep directory each time the MyDEP software is closed.</li>
              <li> complete_database: Export the complete database (database .txt and user_database.txt merged) at the desired location. </li>
              <li> mixture -> Asami-Hanai parameters-> Number of increments: set the number of increments used to calculate the mixture equivalent permittivity using the Asami-Hanai formula. </li>
              </ul>
            </li>
        </ul>
        </li>
        <li> Interface
        <ul><li> Print: Print the interface using the printer. From this menu a pdf can be generated directly (on macOS) or by using a pdfPrinter.</li>
            <li> Export: Open a popupmenu for exporting the interface as displayed in the following image. The following parameters can be choosen:
              <ul>
                <li>	Output format: A5 to A0 or personalized by specifying the width and height.
                </li>
                <li> Resolution: 75, 150, 300 or 600 dpi.
                </li>
                <li> Orientation.
                </li>
                <li> Keep screen aspect ratio: keep the same aspect ratio as what is displayed on the screen. This option will partially rule out the output format chosen. Only one dimension will be conserved.
                </li>
                <li> File format: pdf, jpg, bmp, gif, png, jpeg.
                </li>
              </ul>
              <br>
              <div class="DIVimage">
                  <img class="im" src='/assets/img/image15_Interface_export_parameters.png' />
              </div>
           </li>

        </ul>
        </li>

        <li> Graph
        <ul><li> Undock windows: This option allows to separate the myDEP interface in 3 parts:
              <ul>
                <li>The parameters part containing the left part of the interface (Medium/Frequencies/Model)</li>
                <li>Graphs</li>
                <li>Results and Display options</li>
              </ul>
            <p>Closing  the Graphs or Results and Display parts will redock them all together.</p></li>
            <li> Print: Print the graph displayed on the screen using the printer. From this menu a pdf can be generated directly (on macOS) or by using a pdfPrinter </li>
            <li> Export: Open a popupmenu for exporting the graph displayed on the screen. The following parameters can be choosen:
              <ul>
                <li> Output format (A5 to A0 or personalized by specifying the width and height.</li>
	              <li> Resolution: 75, 150, 300 or 600 dpi.</li>
                <li> Orientation. </li>
                <li> Keep screen aspect ratio: keep the same aspect ration as what is displayed on the screen. This option will partially rule out the output format chosen. Only one dimension will be conserved.</li>
                <li> File format: pdf, jpg, bmp, gif, png, jpeg. </li>
              </ul>
            </li>
            <li> Grid and labels parameters: already explained in the Graph section</li>
            <li> Legend parameters: already explained in the Graph section</li>
        </ul>
        </li>
        <li> Help </li>
        </ul>


 </details>
 </details>
<details>
<summary><h2 class="menutitle"> Database </h2></summary>


<p class="retrait">MyDEP allows to work with cell models from the Homogeneous particle model up to a Four-shell particle model, spherical or ellipsoidal. A database, compiling data for each model that were found in the literature has been created. This database is in the file database.txt. </p>

<p class="retrait">For each model all the information concerning the model can be seen by Clicking on the View references button. The popup menu that open contains:
<ul>
    <li> The Name of the model</li>
    <li> The Author </li>
    <li> The Title of the Article </li>
    <li>The journal where the data were published </li>
    <li> The DOI or link where the article can be found (For a given DOI_ex, the article can be found at dx.doi.org/DOI_ex </li>
    <li> The year of publication </li>
    <li> Remarks: if additional comments are needed </li>
</ul>
<br>
<div class="DIVimage">
    <img class="im" src='/assets/img/image16_ViewReferences.png' />
</div>
</p>

<p class="retrait">The users can either use the model already implemented in the database or create their own. To do so, click on the "Create" button in the desired model type, specify the name of the model and any additional information. Replace the values already present in the interface by the desired ones and click on Save. The saved model will be automatically saved in the user database once the MyDEP software will be closed. The model from the user database can also be deleted by clicking on the Delete button.

A similar principle is applied for the different media in the medium section of MyDEP. For each medium "name" and "Remarks" field are available through the "View" button.</p>


 </details>
<details>
<summary><h2 class="menutitle">Single shell: electrical model </h2></summary>

<p>For the Single-shell model an additional feature allows to specify different properties of the cell membrane: either the "Classical Model" ($th_{cm}$, $\sigma_{cm}$ and $\varepsilon_{cm}$) or the "Electrical Model" (specific membrane conductance $G_{cm}$ and capacitance $C_{cm}$). </p>

<p>
<ul>
    <li>From "Classical Model" to "Electrical Model":<br>
    If the "Classical Model" is selected, a click on the "Convert" button will calculate $G_{cm}$  and $C_{cm}$ following the formula:
    $$G_{cm}=\frac{\sigma_{cm}}{th_{cm}}$$
    $$C_{cm}=\frac{\varepsilon_{cm}}{th_{cm}}$$
    A click on "Electrical Model" will use the calculated values.<br>
    </li>
    <li>
    From "Electrical Model" to "Classical Model":<br>
    If the "Electrical Model" is selected, a click on the "Convert" button will make the $th_{cm}$ box accessible. Once the value is entered, press the "ok" button. The values of $\sigma_{m}$ and $\varepsilon_{cm}$ will be calculated.
    A click on "Classical Model" will use the calculated values.
    </li>
</ul>
</p>

</details>
<details>
<summary><h2 class="menutitle">Specificities of the "homogeneous" particle model </h2></summary>


<p>
The "classical model" uses the electrical properties of the particles, $\sigma_p$ and $\varepsilon_p$, for the calculation of the CM factor, Permittivity, Conductivity and Crossover frequencies (see "Graphs" section). The radius of the particle is only used for the calculation of $F_{DEP}/\nabla E^2_{RMS}$ and $\Gamma_{ROT}/|E^2| $ and, for the ellipsoid, for depolarization factor and all the calculations.

For small particles, surface charges affect significantly their dielectric response and should be taken into account, as shown by the formula:

$$ \sigma_p=\sigma_{p bulk}+\frac{2K_s^i}{r}+\frac{2K_s^d}{r}$$

where<br>
$\sigma_{p bulk}$: bulk electrical conductivity of the particle <br>
$K_s^i$: Stern layer conductance <br>
$K_s^d$: diffuse layer conductance <br>

To account for surface conductance, the user can either specify :
<ul>
  <li> $K_s^i$ and $K_s^d$ </li>
  <li> $K_s^i$ and the zeta potential $\zeta$. </li>
</ul>
</p>
</details>