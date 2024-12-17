# c-project
#include <stdio.h>
float celsiusToFahrenheit(float celsius) {
    return (celsius * 9 / 5) + 32;
}
float fahrenheitToCelsius(float fahrenheit) {
    return (fahrenheit - 32) * 5 / 9;
}
int main() {
    int choice;
    float temperature, convertedTemperature;

    printf("Temperature Converter\n");
    printf("1. Celsius to Fahrenheit\n");
    printf("2. Fahrenheit to Celsius\n");
    printf("Choose an option (1 or 2): ");
    scanf("%d", &choice);

    switch (choice) {
        case 1:
            printf("Enter temperature in Celsius: ");
            scanf("%f", &temperature);
            convertedTemperature = celsiusToFahrenheit(temperature);
            printf("%.2f Celsius is %.2f Fahrenheit\n", temperature, convertedTemperature);
            break;
        case 2:
            printf("Enter temperature in Fahrenheit: ");
            scanf("%f", &temperature);
            convertedTemperature = fahrenheitToCelsius(temperature);
            printf("%.2f Fahrenheit is %.2f Celsius\n", temperature, convertedTemperature);
            break;
        default:
            printf("Invalid choice! Please select 1 or 2.\n");
            break;
    }
    return 0;
}
