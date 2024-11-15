---
layout: default
title:  Getting started
permalink: /getting_started/
---

<h1> Getting started </h1> 
<details>
<summary><h2 class="menutitle"> Introduction</h2></summary>

<p class="retrait"> MyDEP is a Java based standalone software which allows to study dielectric particle response to AC electric fields and to analyse the electric properties of biological cells.
It consists of a Graphical User Interface (GUI) supporting a literature-based database. This tool can also be used with the user's own data sets. </p>
</details>
 
<details>
<summary><h2 class="menutitle"> Installation and system requirements </h2></summary>

<p> MyDEP can be run on Windows, Mac OS X or Linux/Ubuntu operating systems. It requires Java to be installed on your system. Please check you have the latest recommended version of Java installed on your computer. Otherwise it can be downloaded <a href="https://java.com/en/download">here</a> (October 2024: Version 8 Update 431). </p>
<p> Download the latest version of MyDEP by clicking on the <b>Free download from Zenodo</b> button in the page header. Unzip the folder (zip archive) and open it. Double-click on the MyDEP.jar file.</p>

<p> <b>Warning</b>: Sometimes, the default program to open MyDEP.jar is not Java. In this case you need to set Java as the default program to open the .jar files.</p>

<details><summary class="tab"><h3 class="menutitle"> For Mac OS X users </h3> </summary>
<p> For Mac OS X users, depending on the security preferences, the message from Fig.1 might be displayed.</p>

<div class="DIVimage60">
    <img class="im" src='/assets/img/image01_mac.png' />
	<figcaption class="figcap">Fig.1 Popop menu explaining that MyDEP can't be opened (on Mac).
    	</figcaption>
</div>
<p>In this case click on OK, go to System Preferences -> Security and Privacy. Under the General tab the following info should appear Fig.2.</p>

<div class="DIVimage60">
    <img class="im" src='/assets/img/image02_mac.png' />
	<figcaption class="figcap">Fig.2 How to allow the opening of MyDEP.
    	</figcaption>
</div>

<p> Click on "Open anyway" -> Open </p> (Fig.3).

<div class="DIVimage60">
    <img class="im" src='/assets/img/image03_mac.png' />
	<figcaption class="figcap">Fig.3 New popup menu after modifying the security preferences.
    	</figcaption>
</div>
  </details>

<p> The "mydep.ini" file will be created containing all your preferences and the window from MyDEP as displayed in Fig.4 will appear.</p>

<div class="DIVimage">
    <img class="im" src='/assets/img/image04_MyDEP.png' />
	<figcaption class="figcap">Fig.4 MyDEP interface after start up.
    	</figcaption>
</div>

 </details>
<details>
<summary><h2 class="menutitle"> User interface structure </h2></summary>

<div class="DIVimage">
    <img class="im" src='/assets/img/image05_MyDEP_cadreRouge_number_menubar.png' />
	<figcaption class="figcap">Fig.5 Different parts of the MyDEP interface.
    	</figcaption>
</div>

<p> The interface is constituted of 9 different parts as displayed in Fig.5:</p>
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

<details><summary class="tab"><h4 class="menutitle"> 1. Medium </h4> </summary>
	<p class="retrait"> In this section, the user can choose the dielectric properties of the medium which are $\sigma_m$, the electrical conductivity and $\varepsilon_m$, the relative permittivity.
	An additional box allows to indicate the value of the volume fraction $\phi$. It corresponds to the fraction of the volume of the cells compared to the volume of liquid. This value is needed only for the calculation of the permittivity and conductivity of the suspension of particles with the Maxwell-Garnett and Asami-Hanai methods that are described in <a href="/a_bit_of_theory/#Cell_suspension">Cell suspension</a>.</p>
</details>
  <details><summary class="tab"><h4 class="menutitle"> 2. Frequencies </h4></summary> <p> In this section, the user can choose the start and stop frequencies of the graph as well as the number of points, logarithmically spaced, that will be used. </p>
</details>
  <details><summary class="tab"><h4 class="menutitle"> 3. Model </h4></summary> <p> In this section, the user can choose the particle model that will be implemented. Dielectric particles such as cells are usually represented as concentric shells. For more info see <a href="/a_bit_of_theory/#Cell_modelling">Cell modelling</a>. Here the user can specify the number of layers that will be used. Moreover, the particle shape can be either spherical or ellipsoidal. The possible models are: </p>

  <ul>
      <li> <b>Homogeneous particle:</b> This model corresponds to a completely homogeneous particle. The corresponding interface is displayed in Fig.6.
        <br><br>
        <div class="DIVimage">
            <img class="im" src='/assets/img/image06_homogeneous.png' />
		<figcaption class="figcap">Fig.6 MyDEP with the related "Homogeneous Particle" model menu visible.
    		</figcaption>
        </div><br>
<details><summary class="tab"><h5 class="menutitle"> Specificities of the "Homogeneous Particle" model </h5> </summary>

<p class="retrait"> The "Classical Model" uses the electrical properties of the particles, $\sigma_p$ and $\varepsilon_p$, for the calculation of the CM factor, Complex Permittivity, Permittivity, Conductivity and Crossover frequencies (see "Graphs" section). In the case of spherical particles, the radius of the particle is only used for the calculation of $F_{DEP}/\nabla E^2_{RMS}$ and $\Gamma_{ROT}/|E^2|$. For ellipsoidal particles, it is also used for the calculation of the depolarization factor.</p>

<p class="retrait">Surface charges significantly affect significantly the dielectric response of small particles and should be taken into account, as shown by the formula:

$$ \sigma_p=\sigma_{p bulk}+\frac{2K_s^i}{r}+\frac{2K_s^d}{r}$$

where<br>
$\sigma_{p bulk}$: bulk electrical conductivity of the particle <br>
$K_s^i$: Stern layer conductance <br>
$K_s^d$: Diffuse layer conductance <br>

To account for surface conductance, the user can either specify :
<ul>
  <li> $K_s^i$ and $K_s^d$ </li>
  <li> $K_s^i$ and the zeta potential $\zeta$. </li>
</ul>
</p>
  </details>	            
      </li>
      <li> <b>Single-shell:</b> This model corresponds to a particle with an outside layer. The corresponding interface is displayed in Fig.7. For a cell it typically represents a cytoplasm surrounded by a lipid membrane.
        <br><br>
        <div class="DIVimage">
            <img class="im" src='/assets/img/image07_single.png' />
		<figcaption class="figcap">Fig.7 MyDEP with the related "Single-shell Particle" model menu visible.
    		</figcaption>
        </div><br>

<details><summary class="tab"><h5 class="menutitle"> Single shell: Electrical Model </h5> </summary>
<p class="retrait"> For the Single-shell model an additional feature allows to specify different properties of the cell membrane: either the "Classical Model" ($th_{cm}$, $\sigma_{cm}$ and $\varepsilon_{cm}$) or the "Electrical Model" (specific membrane conductance $G_{cm}$ and capacitance $C_{cm}$). </p>
<p>
<ul>
    <li>From "Classical Model" to "Electrical Model":<br>
    If the "Classical Model" is selected, a click on the <b> Convert </b> button will calculate $G_{cm}$  and $C_{cm}$ following the formula:
    $$G_{cm}=\frac{\sigma_{cm}}{th_{cm}}$$
    $$C_{cm}=\frac{\varepsilon_{cm}}{th_{cm}}$$
    A click on "Electrical Model" will use the calculated values.<br>
    </li>
    <li>
    From "Electrical Model" to "Classical Model":<br>
    If the "Electrical Model" is selected, a click on the <b> Convert </b> button will make the $th_{cm}$ box accessible. Once the value is entered, press the <b> OK </b> button. The values of $\sigma_{m}$ and $\varepsilon_{cm}$ will be calculated.
    A click on "Classical Model" will use the calculated values.
    </li>
</ul>
</p>
  </details>
      </li>
      <li> <b>Two-shell:</b> This model corresponds to a particle with two outside layers. The corresponding interface is displayed in Fig.8. For a cell it corresponds to a cytoplasm surrounded by a cell membrane and a cell wall.
        <br><br>
        <div class="DIVimage">
            <img class="im" src='/assets/img/image08_two.png' />
		<figcaption class="figcap">Fig.8 MyDEP with the related "Two-shell" model menu visible.
    		</figcaption>
        </div><br>
      </li>
      <li> <b>Three-shell:</b> This model corresponds to a cell with one outside layer and a nucleus occupying a significant volume. The corresponding interface is displayed in Fig.9. The order of the layers from the inside to the outside is nucleoplasm, nuclear envelope, cytoplasm and cell membrane.
        <br><br>
        <div class="DIVimage">
            <img class="im" src='/assets/img/image09_three.png' />
		<figcaption class="figcap">Fig.9 MyDEP with the related "Three-shell" model menu visible.
    		</figcaption>
        </div><br>
      </li>
      <li> <b>Four-shell:</b> This model corresponds to a cell with two outside layers and a nucleus occupying a significant volume. The corresponding interface is displayed in Fig.10. The order of the layers from the inside to the outside is nucleoplasm, nuclear envelope, cytoplasm, cell membrane and cell wall.
        <br><br>
        <div class="DIVimage">
            <img class="im" src='/assets/img/image10_four.png' />
		<figcaption class="figcap">Fig.10 MyDEP with the related "Four-shell" model menu visible.
    		</figcaption>
        </div><br>
      </li>
  </ul>  

  <p>Here is a summarized description of the implemented cell models (the four-shell model is not represented):</p>
  <div>
      <img class="im" src='/assets/img/image11_CellModel.png' />
		<figcaption class="figcap">Fig.11 Illustration of the different spherical and ellipsoidal cell and particle models implemented in the interface. All the models "Homogeneous sphere", "Single-shell", "Two-shell" and "Three-shell" are illustrated with an example. The implemented "Four-shell" model is not illustrated here.
    		</figcaption>
  </div>

  </details>
  <details><summary class="tab"><h4 class="menutitle"> 4. Sweep </h4></summary> <p class="retrait"> The <b> Sweep </b> button, once pressed, performs a sweep on different values of the selected parameter. To change the parameter on which the sweep is performed, click on the Sweep parameter and select the desired parameter (cf following image). The number of points used, as well as the min and max values, can also be specified. If the log button is pressed, the values will be logarithmically distributed (linearly distributed otherwise). </p>
  <div class="DIVimage60">
      <img class="im" src='/assets/img/image12_SweepParameters.png' />
		<figcaption class="figcap">Fig.12 Illustration of the Sweep button. When pressed the parameter to sweep become visible as well as the min and max values for the sweep.
    		</figcaption>
  </div>

  </details>
  <details><summary class="tab"><h4 class="menutitle"> 5. Calculate </h4></summary> <p class="retrait"> The <b> Calculate </b> button performs the corresponding calculation displayed in the Graphs section. The orange color of the button indicates that no calculation has been performed. The button turns green once the calculation is done.</p>
	<p class="retrait">If the Sweep button is pressed, the progression of the calculation will be displayed on this button by using a progress bar.</p>

  </details>
  <details><summary class="tab"><h4 class="menutitle"> 6. Graphs </h4></summary> <p class="retrait"> The graphs displayed in this section are the following:</p>
	<ul>
    <li> Clausius-Mossotti factor, abbreviated CM factor (real and/or imaginary part).</li>
    <li> Complex Permittivity:
	<ul>
          <li> $|\varepsilon_{eq}^{\ast}| / \varepsilon_{0}$: the modulus of the equivalent complex relative permittivity of the particle. </li>
          <li> $|\varepsilon_{m}^{\ast}|/ \varepsilon_{0}$: the modulus of the complex relative permittivity of the medium. </li>
          <li> $|\varepsilon_{mix}^{\ast}| /  \varepsilon_{0}$: the modulus of the equivalent complex relative permittivity of the particles in suspension in the medium. </li>			
        </ul>  		
		</li>
    <li> Permittivity: 
        <ul>
          <li> $\varepsilon_{eq}$: the equivalent relative permittivity of the particle. </li>
	  <li> $\varepsilon_{m}$: the relative permittivity of the medium. </li>
          <li> $\varepsilon_{mix}$: the equivalent relative permittivity of the particles in suspension in the medium at the given volume fraction.</li>
        </ul>  
    </li>    
    <li> Conductivity:
        <ul>
          <li> $\sigma_{eq}$: the equivalent electrical conductivity of the particle. </li>
	  <li> $\sigma_{m}$: the electrical conductivity of the medium. </li>
          <li> $\sigma_{mix}$: the equivalent electrical conductivity of the particles in suspension in the medium at the given volume fraction.</li>
        </ul>  
    </li>
    <li>Crossover: this graph corresponds to the different crossover frequencies when the sweep mode is performed on $\sigma_{m}$.
    </li>
  </ul>

  <p> <b>Editing curves:</b></p>
  <ul>
      <li> <b>Zooming</b>:<br> You can zoom the graph using the scroll-wheel of your mouse or the zoom functionality of your trackpad. </li>
      <li> <b>Curve properties: </b><br>
      A left click on a displayed curve will select the curve which will appear in a thicker linestyle. The corresponding parameters used for its creation will be displayed in the left part of the interface (Medium/Frequencies/Model).<br>
      A right click on a displayed curve will cause a popup menu to appear with the following options:      
      <ul>
        <li>Curve parameters: The line style of the curve and its width can be adjusted as well as its color with Swatches, HSV, HSL, RGB and CMYK color models. Each point of the curve can also be represented by a marker for which the type and size can be adjusted.</li>
        <li> Sweep curve parameters:
         If the curve was generated in the Sweep mode (sweep of one parameter), this menu enables to modify the line style, line width and color of all the curves generated during the sweep. </li>
        <li> Delete curve: Delete the specific curve. </li>
      </ul>
      </li>
      <li> <b>Legend:</b><br>
      The legend can be moved in the graph by dragging it. The following parameters can be modified by right-clicking on the legend -> Legend parameters:
      <ul>
      <li> Opacity of the legend: By default, the legend background is opaque but can become transparent by unclicking the <b> Opaque </b> button.</li>
      <li> Anchoring (horizontal and vertical): This corresponds to the fixed point when the MyDEP interface size is modified on screen or printed. </li>
      <li> Font and font size </li>
      <li> Font color and Background color</li>
      </ul><br>
      <div class="DIVimage">
          <img class="im" src='/assets/img/image13_LegendParameters.png' />
		<figcaption class="figcap">Fig.13 Popup menu corresponding to the Legend parameters. The label position, Font, Font size and color as well as the Background color can be selected.
    		</figcaption>
      </div>
      <br>
      In the Sweep mode the legend will display the properties of the last generated curve (default mode) or the selected curve.
      </li>
      <li> <b>Axis properties:</b><br>
      A right click on the axes will give access to the Grid and labels parameters menu. This menu offers the possibility to change:
      <ul>
      <li> The displayed axis properties: horizontal and vertical axis labels (possibility to use html for special characters), the font and the font size</li>
      <li> The unit properties: font and font size. </li>
      <li> The major grid and minor grid parameters: line style, line width and color.</li>
      </ul><br>
      <div class="DIVimage">
          <img class="im" src='/assets/img/image14_GridProperties.png' />
		<figcaption class="figcap">Fig.14 Popup menu corresponding to the Label and Grid properties. The label displayed for the x and y axes can be defined as well as the Font and Font size for the Label and the Units. All the parameters of the grid can be selected.
    		</figcaption>
      </div>
      <br>
      </li>
</ul>
     </details>
     
  <details><summary class="tab"><h4 class="menutitle"> 7. Results </h4> </summary><p class="retrait"> This section corresponds to an analysis of part of the graphs. The part is different depending on the selected graph:</p>
<ul>
        <li>CM factor tab:
          <ul>
          <li> <b> Re[CM(f)] </b> and <b> Im[CM(f)] </b> button: If pressed the corresponding curves will be displayed.</li>
          <li> <b> Min Max auto </b> button: If pressed the Min and Max values will be adjusted automatically. Otherwise they will correspond to yAxis<sub>min</sub> and yAxis<sub>max</sub>.</li>
          <li>  <b> f<sub>cursor</sub> </b> button: a vertical line will be displayed at the frequency written in the box, whose unit can be adjusted (Hz, kHz, MHz or GHz). The value can also be adjusted with the corresponding slider. The values of $Re[CM(f)]$, $Im[CM(f)]$, $F_{DEP}/\nabla E^2_{RMS}$ and $\Gamma_{ROT}/|E^2|$ are displayed in the <i> At f<sub>cursor</sub> </i> box.</li>
          <li> <b> Baseline </b> button: A horizontal line will be displayed at the value written in the box. The value can also be adjusted with the corresponding slider.</li>
          <li> <b> Legend </b> button: A click on the Legend button will open a popup menu where the properties to display will be available by ticking the corresponding tickbox. The order of the displayed parameters can be modified by clicking on the corresponding arrows. The "user text" box can be used to display the desired text, using html language when needed.</li>
          <li> Re Crossover: the different crossover frequencies correspond to the frequencies at which $Re[CM(f)] = 0$</li>
	  <li> Im MinMax: the frequencies at which $Im[CM(f)]$ is minimal and maximal</li>
          </ul>
        </li>
        <li> Complex Permittivity, Permittivity and Conductivity tabs:
          <ul>
            <li> <b> Particle </b>, <b> Medium </b> and <b> Mixture </b>buttons: If pressed the corresponding curves will be displayed. </li>
            <li> <b> Min Max auto </b> button: If pressed the Min and Max values will be adjusted automatically. Otherwise, they will correspond to $|\varepsilon_{eq}^{\ast}| / \varepsilon_{0min}$ and $|\varepsilon_{eq}^{\ast}| / \varepsilon_{0max}$
(respectively $\varepsilon_{min}$ and $\varepsilon_{max}$ and $\sigma_{min}$ and $\sigma_{max}$).</li>		  
            <li> <b> f<sub>cursor</sub></b>: A vertical line will be displayed at the frequency written in the box, whose unit can be adjusted (Hz, kHz, MHz or GHz). The value can also be adjusted with the corresponding slider. The values for the Particle, Medium and Mixture are displayed in the <i> At f<sub>cursor</sub></i> box.</li>
            <li> All the other buttons have similar behavior as described in the CM factor tab.</li>
          </ul>
        </li>
        <li> Crossover tab: If a sweep is performed on the $\sigma_{m}$ button, the corresponding crossover frequencies will be displayed in this graph:
		<ul>
		<li> <b> Lower </b> and <b> Upper </b>: If pressed the corresponding curves will be displayed. </li>
    		<li> <b> Min Max auto </b> button: If pressed the Min and Max values will be adjusted automatically. Otherwise, they will correspond to Frequency<sub>min</sub> and Frequency<sub>max</sub>. </li>
          	<li> <b> &sigma;<sub>m</sub> (S/m)</b> button: A vertical line will be displayed at the value written in the box. The value can also be adjusted with the corresponding slider.</li>
            	<li> <b> f<sub>cursor</sub></b>: A horizontal line will be displayed at the frequency written in the box, whose unit can be adjusted (Hz, kHz, MHz or GHz). The value can also be adjusted with the corresponding slider. The values of the Lower and Upper crossover frequencies are displayed in the <i>At &sigma;<sub>m</sub></i> box.</li>
<li> Remark: If both the <b> &sigma;<sub>m</sub> (S/m)</b> and <b> f<sub>cursor</sub></b> buttons are pressed, a click on a point will move the two cursors together. Draging the $\sigma_{m} (S/m)$ cursor on the graph will move both cursors on the same curve.</li>	
		</ul>	
      	</li>    
</ul>
</details>
	
<details><summary class="tab"><h4 class="menutitle"> 8. Display options </h4></summary>
      <p> This section contains different buttons to adjust the properties of the graphs displayed in the Graphs section:</p>
      <ul>
      	 <li> <b> Clear fig </b> button: Clear fig removes all curves from the Graph section.</li>
         <li> <b> X Log </b> button: If X Log is pressed the x axis will be displayed with a logarithmic scale, otherwise with a linear scale.</li>
         <li> <b> Y Log </b> button: If Y Log is pressed the y axis will be displayed with a logarithmic scale, otherwise with a linear scale.</li>
         <li> <b> Hold on </b> button: Hold on retains plots in the current axes so that new plots added to the axes do not delete existing plots.</li>
         <li> <b>Reset zoom</b> button: Reset zoom resets the graph to its initial zoom.</li>
         <li> <b> Legend </b> button: Legend displays the legend in the graph.</li>
      </ul>
      </details>
  
  <details><summary class="tab"><h4 class="menutitle"> 9. Menu bar </h4></summary> <p>The menu bar contains different categories:</p>
<ul>
        <li>File
		<ul><li>Quit: This quits closes the interface.</li></ul></li>
        <li>Database
		<ul>
			<li>Search: This opens a popup menu where all data from the database are visible. This menu is accessible with a keyboard shortcut: Ctrl + F (Windows) or Cmd + F (Mac).It is possible to look at the database for a specific model by long at Name, Author, Title, Journal and Year. A click on the desired model will display the corresponding values in the model part of the interface.</li>
			<li>Import: This imports a new database in the following formats: </li>
				<ul> 
					<li> Tab-separated database </li>
	 				<li> SQLite database </li>
				</ul> 
			<li>Export: This exports a database in the following format</li>
				<ul> 
					<li> Tab-separated database: This exports at the desired location in .txt file:</li>
						<ul> 
							<li> Full user database: This saves the full user database at the desired location.</li>
							<li> Initial database: This saves the initial database provided with MyDEP at the desired location.</li>
						</ul> 	
	 				<li> SQLite database: This exports at the desired location in .db file: </li>
						<ul> 
							<li> Partial user database: This opens a popup menu where the user can select the created models he wants to export.
								<ul>
									<li> <b> Save </b> button: This saves the database at the desired location.</li>
									<li> <b> Save and submit </b> button: The database will be saved at the desired location and an email will be generated from the user mailbox. Please add the references of the paper(s) to help to MyDEP admin to check and add the model to the initial database for all the users.</li>
									<li> <b> Cancel</b> button: This cancels the export.</li>
								</ul> </li>	
							<li> Full user database: This saves the full user database at the desired location.</li>
	 						<li> Initial database: This saves the initial database provided with MyDEP at the desired location.</li>
						</ul> 
				</ul> 
			<li>Download database from GitHub: This downloads the initial database from the MyDEP GitHub page.</li>
			<li>Check for database updates at startup: This checks if a new version of the initial database is available online at startup.</li>
		</ul></li>
	<li> Interface
		<ul>
			<li>Undock windows: This option allows to separate the myDEP interface in 3 parts:
				<ul>
                				<li>The parameters part containing the left part of the interface (Medium/Frequencies/Model).</li>
                				<li>Graphs.</li>
                				<li>Results and Display options.</li>
				</ul>
           			<p>Closing the Graphs or Results and Display parts will redock them all together.</p>
			</li>
        			<li> Print: Print the interface using the printer. From this menu a pdf can be generated directly (on macOS) or by using a pdfPrinter.</li>
			<li> Export</li>
           		<li> Export: This opens a popup menu for exporting the interface as displayed in the following image. The following parameters can be chosen:
             	 		<ul>
                				<li> Output format: A5 to A0 or personalized by specifying the width and height.</li>
                				<li> Resolution: 75, 150, 300 or 600 dpi.</li>
                				<li> Orientation.</li>
                				<li> Keep screen aspect ratio: This keeps the same aspect ratio as what is displayed on the screen. This option will partially rule out the output format chosen. Only one dimension will be conserved.</li>
                				<li> File format: jpg, bmp, gif, png, jpeg.</li>
              			</ul>
              				<div class="DIVimage">
                  			<img class="im" src='/assets/img/image15_Interface_export_parameters.png' />
					<figcaption class="figcap">Fig.15 Popup menu for the export of MyDEP interface. The output format, resolution and file format can be selected.
    					</figcaption> 
             		 		</div>
			</li> 
		</ul>
        </li>
	<li> Graphs
		<ul>
            		<li> Print: This prints the graph displayed on the screen using the printer. From this menu a pdf can be generated directly (on macOS) or by using a pdfPrinter </li>
			<li> Export</li>
				<ul>
					<li>Image: This opens a popup menu for exporting the graph displayed on the screen. The following parameters can be chosen:
						<ul>
                					<li> Output format: A5 to A0 or personalized by specifying the width and height.</li>
	              					<li> Resolution: 75, 150, 300 or 600 dpi.</li>
                					<li> Orientation. </li>
               		 				<li> Keep screen aspect ratio: This keeps the same aspect ratio as what is displayed on the screen. This option will partially rule out the output format chosen. Only one dimension will be conserved.</li>
                						<li> File format: jpg, bmp, gif, png, jpeg. </li>
              					</ul>
					</li>
					<li>CSV: This exports the selected parameters
						<ul> 
							<li> Crossover frequencies: Frequencies and conductivities of each crossover frequencies points displayed in the Crossover tab </li>
							<li> Other: CM factor (Real and Imaginary parts), Complex Permittivity, Permittivity and Conductivity for the particle, the medium and the suspension displayed in the related tabs. The legend can be displayed in the first line of the CSV file if selected.</li>
              					</ul>
					</li>
              					<div class="DIVimage">
                  				<img class="im" src='/assets/img/image18_ExportCSV.png' />
						<figcaption class="figcap">Fig.16 Popup menu to export the different graphs generated by MyDEP.
    						</figcaption>
             		 			</div>
				</ul> 
			<li>Import CSV curve</li>
				<p> MyDEP allows to import a CSV file </p>
              					<div class="DIVimage">
                  				<img class="im" src='/assets/img/image19_ImportCSV.png' />
						<figcaption class="figcap">Fig.17 Popup menu to import in the interface experimental data.
    						</figcaption>
             		 			</div>
		</ul> </li>
	<li> Tools
		<ul>
			<li>Mixture parameters</li>
				<ul>
					<li>Asami-Hanai parameters</li>
						<ul>
							<li> Number of increments: This sets the number of increments used to calculate the mixture equivalent permittivity using the Asami-Hanai formula. </li>
						</ul>
				</ul> 
            		<li> Grid and labels parameters: Already explained in the Graph section.</li>
           		<li> Legend parameters: Already explained in the Graph section.</li>
           		<li> Check for MyDEP updates at startup: This checks if a new version of MyDEP is available online at startup.</li>
		</ul> </li>
	<li> Help
		<ul>
			<li>Online resources: This brings the user to the MyDEP GitHub page.</li>
			<li>About MyDEP: This opens a popup menu where the MyDEP version number, the MYDEP Database version number as well as the Java version are displayed. </li>
			<li>About MyDEP licensing: This opens a popup menu where the MyDEP licence is displayed.</li>
			<li>Contact: This opens a popup menu where the contact address of the MyDEP admin is displayed. The <u> Open in mail client </u> link will open the mail client and prepare an email with the contact address.</li>
		</ul> </li>
</ul>

 </details>
 </details>
<details> <summary><h2 class="menutitle"> Database </h2></summary>


<p class="retrait"> MyDEP allows to work with cell models from the Homogeneous particle model up to a Four-shell particle model, spherical or ellipsoidal. A database, compiling data for each model that was found in the literature has been created. This database is in the file mydep_database.db. To quickly access and explore the database, press Ctrl + F (Windows) or Cmd + F (Mac).</p>

<p class="retrait">For each model all the information concerning the model can be seen by clicking on the View references button. A popup menu will open containing the following fields:
<ul>
    <li> The Name of the model</li>
    <li> The Author </li>
    <li> The Title of the Article </li>
    <li>The journal where the data were published </li>
    <li> The DOI or link where the article can be found (For a given DOI_ex, the article can be found at dx.doi.org/DOI_ex)</li>
    <li> The year of publication </li>
    <li> Remarks: if additional comments are needed </li>
</ul>
<br>
<div class="DIVimage">
    <img class="im" src='/assets/img/image16_ViewReferences.png' />
	<figcaption class="figcap">Fig.18 Popup menu after a click on the View References button.
    	</figcaption>
</div>
</p>

<p class="retrait">The users can either use the model already implemented in the database or create their own. To do so, click on the <b> Create </b> button in the desired model type, specify the name of the model and any additional information. Replace the values already present in the interface by the desired ones and click on the <b> Save </b> button. The saved model will be automatically saved in the user database once the MyDEP software will be closed. The model from the user database can also be deleted by clicking on the <b> Delete </b> button.</p>

<p class="retrait"> A similar principle is applied for the different media in the medium section of MyDEP. For each medium "Name" and "Remarks" fields are available through the <b>View</b> button.</p>

<p class="retrait"> To suggest a new element to the MyDEP admin for the database, click the menu Database -> Export -> SQLlite database -> Partial user database. Add the element from the "User database" column to the "Database to export" column. Then click on the <b> Save and submit</b> button. A popop menu will appear on the screen proposing to save the file as "mydep_partialuserdatabase.db". Click on the <b> Save </b> button. Your mail client will open and a draft email will be generated to the contact address. Please add the reference of the suggested model. Do not forget to attach the "mydep_partialuserdatabase.db" file. The MyDEP admin will review your suggestion and add it to the initial database distributed to all users afterwards.</p>

 </details>

<style>
	/*getting started css*/
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
/*******************/
</style>
