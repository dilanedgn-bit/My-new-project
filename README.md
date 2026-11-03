
# Smart Energy Optimizer for Homes

Final project for the Building AI course

## Summary

The Smart Energy Optimizer is an AI-powered system designed to predict daily household solar power generation and optimize energy consumption. By analyzing local weather forecasts and historical energy consumption data, it suggests the best times to run heavy appliances (like washing machines or EV chargers) to maximize self-consumption and reduce electricity costs.

## Background

Energy prices are fluctuating, and many homeowners with solar panels struggle to optimize their self-consumption efficiently. Manual planning is difficult because power production depends heavily on unpredictable weather conditions.

* **Problem 1:** Inefficient use of self-generated solar power leading to unnecessary grid electricity purchases.
* **Problem 2:** Lack of automated insights on when to run high-energy household devices.
* **Personal Motivation:** Managing home energy efficiently sparked my interest in using machine learning to automate energy scheduling and promote green energy usage.

## How is it used?

The system is integrated into a smart home dashboard or mobile application.

* **Context:** Used by homeowners with solar panels and smart home systems.
* **Users:** Individuals looking to lower their electricity bills and carbon footprint.

### How it works:
1. Weather Forecast Integration: Collects temperature, cloud cover, and solar irradiance predictions.
2. Production Prediction: Predicts hourly solar output for the upcoming 24 hours.
3. Consumption Pattern Analysis: Analyzes historical user consumption habits.
4. Recommendation Engine: Generates an optimized schedule for household appliances.

```python
# Simple demonstration of calculating predicted solar output based on efficiency and irradiance
def predict_solar_output(irradiance, panel_area, efficiency=0.18):
    """
    Calculates predicted solar power output in kWh.
    irradiance: Solar irradiance in kW/m²
    panel_area: Total area of solar panels in m²
    efficiency: Solar panel efficiency factor (default 18%)
    """
    return irradiance * panel_area * efficiency

# Example usage
predicted_kwh = predict_solar_output(irradiance=0.85, panel_area=25)
print(f"Predicted Output: {predicted_kwh:.2f} kWh")


