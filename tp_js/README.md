# JavaScript Exercises

## Exercise 1: Temperature Conversion

**Description:**
This exercise implements a function called `degreC()` that converts a given temperature from Fahrenheit to Celsius using the formula:

\[ \text{tempC} = \frac{5}{9} (\text{tempF} - 32) \]

The function prompts the user to enter a temperature in Fahrenheit and then displays the equivalent temperature in Celsius.
```
<script>
        function degreC() {
            let tempF = prompt("Entrez une température en degrés Fahrenheit :");
            tempF = parseFloat(tempF);

            if (!isNaN(tempF)) {
                let tempC = (5 / 9) * (tempF - 32);
                alert(`La température en degrés Celsius est : ${tempC.toFixed(2)}°C`);
            } else {
                alert("Veuillez entrer un nombre valide.");
            }

        }
        degreC()
    </script>
```

**Example:**
![image_alt](https://github.com/FatihaELHABTI/web_tps/blob/main/tp_js/ex1s1.PNG)
![image_alt](https://github.com/FatihaELHABTI/web_tps/blob/main/tp_js/ex1s2.PNG)


---

## Exercise 2: Time Conversion

**Description:**
This exercise defines a function called `hjms()` that converts a given number of seconds into days, hours, minutes, and seconds. The function prompts the user for input and displays the result.

**Conversion Rules:**
- 1 day = 24 hours
- 1 hour = 60 minutes
- 1 minute = 60 seconds
```
 <script>
        function hjms() {
                let totalSeconds = prompt("Entrez un nombre de secondes :");
                totalSeconds = parseInt(totalSeconds);

                if (isNaN(totalSeconds) || totalSeconds < 0) {
                    alert("Veuillez entrer un nombre valide.");
                    return;
                }

                let jours = Math.floor(totalSeconds / (24 * 3600));
                let reste = totalSeconds % (24 * 3600);
                let heures = Math.floor(reste / 3600);
                reste %= 3600;
                let minutes = Math.floor(reste / 60);
                let secondes = reste % 60;

                alert(`${jours} jours, ${heures} heures, ${minutes} minutes, ${secondes} secondes`);
            }

            // Appel de la fonction
            hjms();

    </script>
```


**Example:**
![image_alt](https://github.com/FatihaELHABTI/web_tps/blob/main/tp_js/ex2s1.PNG)
![image_alt](https://github.com/FatihaELHABTI/web_tps/blob/main/tp_js/ex2s2.PNG)

## Exercise 3: Improved Time Conversion

**Description:**
This exercise enhances the `hjms()` function by improving the output format:
- Values that are zero are omitted from the display.
- Singular/plural handling (e.g., "1 hour" instead of "1 hours").

**Example:**
![image_alt](https://github.com/FatihaELHABTI/web_tps/blob/main/tp_js/ex3s1.PNG)

```

                if (jours > 0) result.push(`${jours} ${jours === 1 ? "jour" : "jours"}`);
                if (heures > 0) result.push(`${heures} ${heures === 1 ? "heure" : "heures"}`);
                if (minutes > 0) result.push(`${minutes} ${minutes === 1 ? "minute" : "minutes"}`);
                if (secondes > 0) result.push(`${secondes} ${secondes === 1 ? "seconde" : "secondes"}`);

                alert(result.join(", "));
```
---


This project was created as part of JavaScript learning exercises.

