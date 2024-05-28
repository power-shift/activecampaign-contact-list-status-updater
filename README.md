# README

## Purpose

This script updates the status of the provided contacts and their desired list to the "Subscribed" status on ActiveCampaign. This is useful because there is currently no way to perform this task in bulk using the web interface.

## Requirements

- A `contacts.csv` file with `contact_id` and `list_name` per row.
- Each contact should have been previously subscribed to the list (this script is not for importing contacts).
- Chromedriver that matches your Chrome version. You can download it from [here](https://googlechromelabs.github.io/chrome-for-testing/).

## Setup

1. **Prepare the `contacts.csv` file**: Ensure your CSV file is formatted with the following columns:
    ```csv
    contact_id,list_name
    1234,List_A
    5678,List_B
    ```

2. **Install Chromedriver**: Download and install the version of Chromedriver that matches your Chrome browser from [here](https://googlechromelabs.github.io/chrome-for-testing/).

3. **Install Python dependencies**: Ensure you have the following Python libraries installed:
    - `selenium`
    - `csv`

    You can install Selenium using pip:
    ```bash
    pip install selenium
    ```

## Usage

1. **Enter your ActiveCampaign subdomain**: Update the `activecampaign_subdomain` variable in the script with your ActiveCampaign subdomain:
    ```python
    activecampaign_subdomain = 'your_subdomain'
    ```

2. **Initialize and run the script**:

    - Open the script in your Python environment.
    - Run the script.

    The script will:
    - Read the contacts from the `contacts.csv` file.
    - Open a Chrome browser window.
    - Navigate to the ActiveCampaign login page.
    - Allow you to manually log in and complete any required security prompts.
    - Iterate through each contact and update their list status to "Subscribed".

## License
This script is provided “as is”, without warranty of any kind. Use it at your own risk.