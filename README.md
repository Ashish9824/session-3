# session-3

### Task 1: Flipkart Product Variables & Data Types

In C, strings are represented as character arrays (`char[]`), `float` stores single-precision floating-point numbers, and `double` stores double-precision floating-point numbers.

```c
#include <stdio.h>

int main() {
    // Variable declarations and assignments
    char productName[] = "Wireless Bluetooth Headphones"; // String (char array)
    float price = 1499.99f;                               // Float
    double rating = 4.35;                                 // Double

    // Printing values along with their declared data types
    printf("Product Details:\n");
    printf("Product Name [Data Type: char[] / string] : %s\n", productName);
    printf("Price        [Data Type: float]          : ₹%.2f\n", price);
    printf("Rating       [Data Type: double]         : %.2lf\n", rating);

    return 0;
}

```

---

### Task 2: Zomato Order with Constant GST Rate

The `const` keyword prevents the variable from being reassigned or modified after its declaration.

```c
#include <stdio.h>

int main() {
    // Constant GST rate constraint (cannot be modified after initialization)
    const float GST_RATE = 0.18f; // 18% GST

    float basePrice = 350.00f; // Base food order price
    float gstAmount = basePrice * GST_RATE;
    float finalPrice = basePrice + gstAmount;

    printf("--- Zomato Order Summary ---\n");
    printf("Base Food Price : ₹%.2f\n", basePrice);
    printf("GST Applied (18%%): ₹%.2f\n", gstAmount);
    printf("Total Payable   : ₹%.2f\n", finalPrice);

    return 0;
}

```

---

### Task 3: Spotify Playlist Single Formatted Sentence

```c
#include <stdio.h>

int main() {
    char playlistName[] = "Daily Chill Mix";
    int totalSongs = 24;
    float averageDuration = 3.45f; // in minutes

    // Single formatted sentence output
    printf("My favorite Spotify playlist is \"%s\", which has %d songs with an average track duration of %.2f minutes.\n",
           playlistName, totalSongs, averageDuration);

    return 0;
}

```

---

### Task 4: Variable Name Validation & Corrections

Standard C variable naming rules require names to begin with a letter or an underscore (`_`), contain only alphanumeric characters and underscores, and contain no hyphens or special symbols (like `$`).

| Variable Name | Valid / Invalid | Reason | Corrected Version |
| --- | --- | --- | --- |
| **`1stPlayer`** | **Invalid** | Variable names cannot start with a digit. | `firstPlayer` or `player1` |
| **`player_age`** | **Valid** | Starts with a letter, contains only lowercase letters and an underscore. | `player_age` |
| **`$score`** | **Invalid** | The dollar sign (`$`) is a special character and not allowed in standard C identifier naming. | `score` or `playerScore` |
| **`total-marks`** | **Invalid** | Hyphens (`-`) are treated as subtraction operators, not identifier characters. | `total_marks` or `totalMarks` |
| **`userName`** | **Valid** | Follows valid camelCase naming conventions using letters only. | `userName` |
