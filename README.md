#  Chart Bar Implementation

## Description
This HTML file creates a simple bar chart using Chart.js, an open-source JavaScript library for data visualization. The chart dynamically accepts user input for X and Y values, validates the inputs, and displays a bar chart accordingly. It includes basic styling and error handling.

---

## Features
1. **Dynamic User Input**:
   - Prompts the user to input X-axis and Y-axis values as comma-separated strings.
   - Automatically parses and processes the user input.

2. **Error Handling**:
   - Validates if the number of X-values matches the number of Y-values. 
   - Alerts the user if the lengths do not match.

3. **Chart.js Integration**:
   - Displays a bar chart with user-defined data.
   - Configured with basic options such as custom Y-axis scale, background colors, and legend settings.

4. **Styling**:
   - The page has a light pink background (`rgb(250, 230, 247)`).
   - Chart canvas is responsive and dynamically sized with a maximum width of 500px.

---

## Setup Instructions

1. **Dependencies**:
   - The project uses Chart.js v2.9.4. The script is included via a CDN:
     ```
     <script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.9.4/Chart.js"></script>
     ```

2. **Usage**:
   - Open the HTML file in a browser.
   - A prompt will ask for the X-axis values (labels) and Y-axis values (data points).
   - Input the values in a comma-separated format (e.g., `A,B,C` for X-axis and `10,20,30` for Y-axis).
   - Ensure the number of X and Y values is equal; otherwise, an alert will display.

3. **Input Example**:
   - X-axis (labels): `Jan, Feb, Mar, Apr`
   - Y-axis (data): `50, 75, 25, 90`

---

## Code Explanation

### HTML Structure
- The file includes a `<canvas>` element where the Chart.js bar chart is rendered.

### CSS Styling
- Basic styling for the body and chart container is provided:
  - Background color: `rgb(250, 230, 247)`
  - Padding: `150px` for centered appearance.

### JavaScript Logic
- Prompts the user for X and Y values using the `prompt()` function.
- Validates that the length of the X and Y arrays matches.
- Creates a bar chart using the parsed data with these settings:
  - **Type**: `bar`
  - **Labels**: User-provided X values.
  - **Data Points**: User-provided Y values.
  - **Options**:
    - No legend displayed (`legend: {display: false}`).
    - Y-axis scale is fixed between `0` and `100`.

---

## Notes and Limitations

1. **Input Validation**:
   - The script does not handle non-numeric Y-values. Ensure all Y-values are numeric.
   - Trimming is applied to remove extra spaces around values.

2. **Y-Axis Range**:
   - The Y-axis is hardcoded with a minimum of `0` and a maximum of `100`. Modify the `ticks` in the `scales` option if needed.

3. **Chart.js Version**:
   - This script uses Chart.js v2.9.4, which may differ in syntax from newer versions. Ensure compatibility when upgrading.

4. **Responsive Design**:
   - While the chart canvas has a maximum width of `500px`, further improvements can be made for better responsiveness on different screen sizes.

---

Feel free to adapt the code to meet your specific needs!
