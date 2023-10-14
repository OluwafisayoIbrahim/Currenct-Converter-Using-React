# Currency Converter App

This is a simple React.js application that allows you to convert currency from one currency to another using the latest exchange rates.

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Description](#description)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Contributing](#contributing)

## Introduction

This application is built using React.js and Axios to fetch exchange rate data from an external API. It provides a user-friendly interface for entering an amount in one currency and instantly seeing the equivalent amount in another currency based on the fetched exchange rates.

## Features

- Currency conversion from one currency to another.
- Real-time exchange rates fetched from a remote API.
- User-friendly interface with input fields and dropdowns.

## Description
1. Imports: The code starts by importing necessary modules and components. It uses import statements to include the required dependencies:

- App.css for styling.
- CurrencyInput component (assuming it's in a file named CurrencyInput.js).
- React hooks and the Axios library for making API requests.
  
2. Function Component: The code defines a functional component named App. Functional components are a way to create reusable UI elements in React.

3. State Management: Several state variables are declared using the useState hook to manage the application's data:
   
- amount1 and amount2 represent the amounts in the two currencies being converted.
- currency1 and currency2 represent the selected source and target currencies.
- rates stores exchange rates fetched from an API.
  
3. Data Fetching: The useEffect hook is used to make an Axios API request to retrieve exchange rates. It uses the axios.get method to fetch data from a URL and sets the rates in the rates state variable when the data is received. This hook runs once when the component mounts, as indicated by the empty dependency array [].

4. Data Initialization: A second useEffect hook is used to set the initial values for amount1 and amount2 when the rates data becomes available. This is done by calling the handleAmount1Change function with an initial value of 1. The handleAmount1Change function calculates and sets amount2 based on the provided exchange rates.

5. Helper Functions:

- format(number) is a utility function that formats a number to a fixed number of decimal places. It's used to round the calculated amounts.
handleAmount1Change, handleCurrency1Change, handleAmount2Change, and handleCurrency2Change are event handling functions. They update state variables based on user interactions.
Rendering: Inside the return statement, the component renders a simple UI:

- A title, "Currency Converter," is displayed as an <h1> element.
Two instances of the CurrencyInput component are used. Each CurrencyInput represents an input field for currency amount and a dropdown to select the currency. They receive event handling functions and the list of available currencies.

## Prerequisites

Before you begin, ensure you have met the following requirements:

- Node.js and npm installed on your local machine.
- Internet connection to fetch exchange rates from the API.

## Installation

To install and run the application locally, follow these steps:

1. Clone the repository to your local machine:

   ```shell```
   git clone <repository-url>
Navigate to the project directory:

```shell```
cd currency-converter-app
Install the required dependencies:

```shell```
npm install

## Usage
To start the development server and view the application in your browser, run the following command:

```shell```
npm start
The application should open in your default web browser, allowing you to use the currency conversion functionality.

## Configuration
You can configure the API URL and API key in the code if needed. Currently, the application is set to fetch exchange rates from a specific URL.

## Contributing
1. Fork the repository on GitHub.
2. Clone the fork to your local machine.
3. Create a new branch for your feature or bug fix.
4. Make your changes and commit them.
5. Push your changes to your fork on GitHub.
6. Open a pull request to the main repository.
