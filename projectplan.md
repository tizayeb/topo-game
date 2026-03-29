
I need a single-file web application (HTML, CSS, and JavaScript) to create an interactive topology learning game. The goal is for a user to identify locations on a map based on alphanumeric markers.

### 1. Data Configuration
Integrate the following `locationData` into the JavaScript logic:

| ID | Name | ID | Name |
| :--- | :--- | :--- | :--- |
| **A** | Noord-Holland | **11** | Hilversum |
| **B** | Zuid-Holland | **12** | Amersfoort |
| **C** | Utrecht | **13** | Leiden |
| **1** | Amsterdam | **14** | Alphen aan den Rijn |
| **2** | Haarlem | **15** | Zoetermeer |
| **3** | Utrecht (Stad) | **16** | Gouda |
| **4** | Den Haag | **17** | Delft |
| **5** | Den Helder | **18** | Rotterdam |
| **6** | Enkhuizen | **19** | Dordrecht |
| **7** | Alkmaar | **a** | Noordzee |
| **8** | Purmerend | **b** | Waddenzee |
| **9** | Zaandam | **c** | Afsluitdijk |
| **10** | Amstelveen | **d** | IJsselmeer |
| **e** | Markermeer | **f** | Noordzeekanaal |
| **g** | Amsterdam-Rijnkanaal | **h** | Lek |
| **i** | Nieuwe Waterweg | **D** | Texel |
| **E** | Randstad | **F** | Haarlemmermeer |
| **G** | Schiphol | **H** | Rijnmond |
| **AM** | Almere | **DB** | De Bilt |
| **MV** | Maasvlakte | **WF** | West-Friesland |
| **WL** | Westland | | |

### 2. Functional Requirements
* **Infinite Loop:** The game must never end. Once a question is answered, show feedback for 1.5 seconds, then automatically load a new random marker.
* **Map Display:** Display the image named `IMG_9648.JPG`. Ensure it is responsive and occupies the top half of the screen.
* **Input Method:** * Primary: Multiple Choice (5 options). The correct answer plus 4 random distractors from the list.
    * Secondary (Toggleable): A text input box for "Hard Mode."
* **Scorekeeping:** Track the "Current Session Score" and a "Best Streak" (consecutive correct answers).

### 3. Visuals & UI
* Use a clean, modern educational theme (Sans-serif fonts, ample whitespace).
* **Feedback:** Flash the screen/button Green for correct and Red for incorrect.
* **Mobile First:** Ensure buttons are large enough for touchscreens.

### 4. Output Format
* Provide the entire solution in **one single HTML file** containing all CSS and JavaScript.
