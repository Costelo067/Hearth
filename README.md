#include <iostream>
#include <vector>

using namespace std;

// Function to calculate the average heart rate
double calculateAverageHeartRate(const vector<int>& heartRates) {
    int sum = 0;
    for (int rate : heartRates) {
        sum += rate;
    }
    return static_cast<double>(sum) / heartRates.size();
}

int main() {
    // Vector to store heart rates
    vector<int> heartRates;

    // Prompt user to enter heart rates
    cout << "Enter heart rates (enter a negative value to stop):" << endl;

    // Input heart rates until the user enters a negative value
    int heartRate;
    while (true) {
        cout << "Enter heart rate: ";
        cin >> heartRate;
        if (heartRate < 0)
            break;
        heartRates.push_back(heartRate);
    }

    // Calculate the average heart rate
    double averageHeartRate = calculateAverageHeartRate(heartRates);

    // Display the average heart rate
    cout << "Average heart rate: " << averageHeartRate << endl;

    return 0;
}
# Hearth
Human hearth
