# WEEK-2 CAD AND DESIGN: Fundamentals of Aeromodelling

Welcome to Week 2 of the Aeromodelling Club's CAD and Design module. This week, we transition from basic software navigation into the core of aerospace engineering. You will learn the physics of flight, how to source aerodynamic data, how to model physical wings, and how to simulate their performance.

## 1. CAD Basics (Choose Your Software)
Computer-Aided Design (CAD) is the foundation of modern engineering. Before we can analyze a wing, we must be able to translate our mathematical concepts into a 3D environment. 

Choose **one** of the following software packages and complete the introductory playlist. Focus on understanding how to sketch 2D profiles and extrude them into 3D bodies.

*   **SolidWorks (Industry Standard):** Best for rigorous mechanical design and complex assemblies.
    *   [Insert Your SolidWorks Playlist Link Here]
*   **Fusion 360 (Cloud-Based & Beginner Friendly):** Great for rapid prototyping.
    *   [Insert Your Fusion 360 Playlist Link Here]

---

## 2. Aerodynamics Fundamentals: Lift, Drag & Airfoils
To design an aircraft, you must understand the forces acting upon it. The two most critical aerodynamic forces are **Lift** and **Drag**.

### The Airfoil
An airfoil is the 2D cross-sectional shape of a wing. Its specific geometry dictates how air flows around it to generate pressure differentials.
*   **Leading Edge (LE):** The front-most coordinate of the airfoil.
*   **Trailing Edge (TE):** The sharp, rear-most coordinate where airflow rejoins.
*   **Chord Line:** An imaginary straight line connecting the LE and TE. The length of this line is the **Chord ($c$)**.
*   **Camber:** The asymmetry between the top and bottom surfaces. High camber generally produces a higher lift coefficient.
*   **Angle of Attack ($\alpha$):** The angle between the chord line and the oncoming free-stream airflow velocity vector.

### Lift ($L$)
Lift is the force generated perpendicular to the oncoming airflow. It is governed by the following equation:
$$L = \frac{1}{2} \rho v^2 S C_L$$
*(Where $\rho$ = air density, $v$ = free-stream velocity, $S$ = wing planform area, and $C_L$ = Lift Coefficient).*

### Drag ($D$)
Drag is the aerodynamic resistance force acting parallel to the oncoming airflow. Our primary design goal is often to maximize the Lift-to-Drag ratio ($L/D$).
$$D = \frac{1}{2} \rho v^2 S C_D$$
*(Where $C_D$ = Drag Coefficient).*

---

## 3. Navigating Airfoiltools.com
[Airfoil Tools](http://airfoiltools.com/) is an open-source database containing the spatial coordinates and aerodynamic performance data for thousands of airfoils.

### The Reynolds Number ($Re$)
When evaluating airfoil data, you must look at graphs plotted at the correct Reynolds Number. $Re$ is a dimensionless number that dictates the flow regime (laminar vs. turbulent) over the wing. 
$$Re = \frac{\rho v c}{\mu}$$
*(Where $c$ = chord length and $\mu$ = dynamic viscosity of the fluid).*

### Workflow on Airfoiltools
1.  **Search:** Find standard airfoils like `NACA 4412` or `Clark Y`.
2.  **Analyze Polars:** Look at the $C_L$ vs $\alpha$ graph to predict stall angle, and the $C_L/C_D$ vs $\alpha$ graph to find the most aerodynamically efficient angle of attack.
3.  **Download:** Download the **"Selig format dat file"**. This is a raw text file containing the exact $X$ and $Y$ coordinates of the airfoil perimeter, normalized to a chord length of 1.

---

## 4. 3D Wing Design from `.dat` Files
You cannot simulate a 2D text file. We must import the `.dat` coordinates into our CAD software to build the physical geometry.

### The Workflow
1.  **Format the Data:** Open the `.dat` file in Excel or a text editor. CAD software operates in a 3D Cartesian space ($X, Y, Z$). You must add a third column consisting entirely of zeros ($Z=0$) so the software knows where to place the 2D curve.
2.  **Import to CAD:** 
    *   *SolidWorks:* Use `Insert > Curve > Curve Through XYZ Points`, select your formatted file, and a closed curve will appear.
    *   *Fusion 360:* Use an "Import Spline CSV" script.
3.  **Extrude:** Convert the imported curve into a sketch entity and extrude it to your calculated wingspan ($b$).

---

## 5. Aerodynamic Analysis in XFLR5
[XFLR5](http://www.xflr5.tech/xflr5.htm) is an analysis tool specifically built for model aircraft operating at low Reynolds numbers. It uses the XFoil engine to predict wing behavior using potential flow and panel methods.

### The Analysis Workflow
1.  **2D Direct Foil Analysis:** 
    *   Import your raw `.dat` file.
    *   Define your expected Reynolds number based on your target velocity and chord length.
    *   Run a **Batch Analysis**. The software will generate theoretical $C_L$ and $C_D$ polars for your specific airfoil.
2.  **3D Wing Design:**
    *   Open the Wing/Plane design module.
    *   Define your macro geometry: Wingspan, Chord, Sweep angle, and Dihedral.
    *   Map the 2D airfoil you analyzed in Step 1 to this 3D geometry.
    *   Run a 3D analysis (using Lifting Line Theory or Vortex Lattice Method) to visualize the pressure distribution and total lift across the wing.

*   **Watch the Tutorial:** [Insert Your XFLR5 Video/Playlist Link Here]

---

## 🎯 Week 2 Tasks
To complete this week's module, submit the following:

1.  **CAD Setup:** Complete the video playlist for your chosen CAD software.
2.  **Data Sourcing:** Download the Selig `.dat` files for the **Clark Y** and **NACA 2412** airfoils.
3.  **CAD Modeling:** Format your `.dat` file, import the XYZ coordinates into your CAD software, and extrude it to create a solid wing segment with a $150$ mm chord and $300$ mm span.
4.  **Simulation:** Open XFLR5, run a 2D Batch Analysis on both airfoils for $Re = 100,000$ to $300,000$. Create a basic 3D rectangular wing using the airfoil that showed the highest $C_L/C_D$ ratio, and run a 3D analysis at $10$ m/s.