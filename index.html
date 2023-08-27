<!DOCTYPE html>
<html>
<head>
  <title>RRSP Calculator</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 20px;
      background-color: #f7f7f7;
    }

    h1 {
      color: #333;
    }

    p {
      color: #555;
    }

    label {
      display: block;
      margin-bottom: 5px;
      color: #333;
    }

    input, select {
      width: 10%;
      padding: 8px;
      margin-bottom: 15px;
      border: 1px solid #ccc;
      border-radius: 4px;
    }

    button {
      background-color: #007BFF;
      color: #fff;
      padding: 10px 20px;
      border: none;
      border-radius: 4px;
      cursor: pointer;
    }

    button:hover {
      background-color: #0056b3;
    }

    h2 {
      color: #333;
      margin-top: 20px;
    }

    #results {
      color: #007BFF;
      font-size: 18px;
      font-weight: bold;
    }
  </style>
  <script>
    function calculateTax() {
      const income = parseFloat(document.getElementById('income').value);
      const rrspContribution = parseFloat(document.getElementById('rrspContribution').value);
      const province = document.getElementById('province').value;

      // Federal Tax Brackets (as of 2021)
      const federalBrackets = [0, 49020, 98040, 151978, 216511];
      const federalRates = [0.15, 0.205, 0.26, 0.29, 0.33];

      // Provincial Tax Brackets (as of 2021, simplified example)
      const provincialBrackets = {
        "Alberta": [0, 134238, 161086, 214781, 322171],
        "British Columbia": [0, 43070, 86141, 98901, 120094, 162832, 227091],
        "Ontario": [0, 46226, 92454, 150000, 220000],
        "Quebec": [0, 46295, 92580, 112655],
        "Nova Scotia": [0, 29590, 59180, 93000, 150000],
        "Manitoba": [0, 34431, 74416],
        "New Brunswick": [0, 44887, 89775, 145955, 166280],
        "Newfoundland and Labrador": [0, 39147, 78294, 139780, 195693, 250000, 500000, 1000000],
        "Northwest Territories": [0, 45462, 90927, 147826],
        "Nunavut": [0, 47862, 95724, 155625],
        "Prince Edward Island": [0, 31984, 63969],
        "Saskatchewan": [0, 46773, 133638],
        "Yukon": [0, 50197, 100392, 155625, 500000],
      };
      
      // Provincial Tax Rates (as of 2021, simplified example)
      const provincialRates = {
        "Alberta": [0.1, 0.12, 0.13, 0.14, 0.15],
        "British Columbia": [0.0506, 0.077, 0.105, 0.1229, 0.147, 0.168, 0.205],
        "Ontario": [0.0505, 0.0915, 0.1116, 0.1216, 0.1316],
        "Quebec": [0.15, 0.2, 0.24, 0.2575],
        "Nova Scotia": [0.0879, 0.1495, 0.1667, 0.175, 0.21],
        "Manitoba": [0.108, 0.1275, 0.174],
        "New Brunswick": [0.0968, 0.1482, 0.1652, 0.1784, 0.203],
        "Newfoundland and Labrador": [0.087, 0.145, 0.158, 0.178, 0.198, 0.208, 0.213, 0.218],
        "Northwest Territories": [0.059, 0.086, 0.122, 0.1405],
        "Nunavut": [0.04, 0.07, 0.09, 0.115],
        "Prince Edward Island": [0.098, 0.138, 0.167],
        "Saskatchewan": [0.105, 0.125, 0.145],
        "Yukon": [0.064, 0.09, 0.109, 0.128, 0.15],
      };

      // Find the appropriate tax bracket for the given income
      function findBracket(income, brackets) {
        for (let i = 0; i < brackets.length; i++) {
          if (i === 0 && income <= brackets[i]) {
            return i;
          }
          if (income > brackets[i - 1] && income <= brackets[i]) {
            return i;
          }
        }
        return brackets.length - 1;
      }

      // Calculate federal tax
      let federalTax = 0;
      let remainingIncome = income;
      for (let i = 0; i < federalBrackets.length; i++) {
        const taxableIncome = i === 0
          ? Math.min(remainingIncome, federalBrackets[i])
          : Math.min(remainingIncome, federalBrackets[i] - federalBrackets[i - 1]);
        federalTax += taxableIncome * federalRates[i];
        remainingIncome -= taxableIncome;
        if (remainingIncome <= 0) {
          break;
        }
      }

      // Calculate provincial tax
      const provinceBrackets = provincialBrackets[province];
      const provinceTaxRate = provincialRates[province];
      let provincialTax = 0;
      remainingIncome = income;
      for (let i = 0; i < provinceBrackets.length; i++) {
        const taxableIncome = i === 0
          ? Math.min(remainingIncome, provinceBrackets[i])
          : Math.min(remainingIncome, provinceBrackets[i] - provinceBrackets[i - 1]);
        provincialTax += taxableIncome * provinceTaxRate[i];
        remainingIncome -= taxableIncome;
        if (remainingIncome <= 0) {
          break;
        }
      }

      // Calculate tax savings from RRSP contribution
      const rrspTaxSavings = rrspContribution * (federalRates[federalRates.length - 1] + provinceTaxRate[provinceTaxRate.length - 1]);

      // Calculate total tax without RRSP contribution
      const totalTaxWithoutRRSP = federalTax + provincialTax;

      // Calculate total tax with RRSP contribution
      const totalTaxWithRRSP = totalTaxWithoutRRSP - rrspTaxSavings;

      // Display results
      const totalTaxWithoutRRSPElement = document.getElementById('totalTaxWithoutRRSP');
      const totalTaxWithRRSPElement = document.getElementById('totalTaxWithRRSP');
	  const totalTaxSavingsElement = document.getElementById('rrspTaxSavings');
      totalTaxWithoutRRSPElement.textContent = totalTaxWithoutRRSP.toFixed(2);
      totalTaxWithRRSPElement.textContent = totalTaxWithRRSP.toFixed(2);
	  totalTaxSavingsElement.textContent = rrspTaxSavings.toFixed(2);

      // Display the results section
      const resultsSection = document.getElementById('results');
      resultsSection.style.display = 'block';
    }
  </script>
</head>
<body>
  <h1>RRSP Calculator</h1>
  <p>输入您的年收入、RRSP（退休储蓄计划）存款，并选择您的省份/地区以计算税款。</p>
  <p>Enter your annual income, RRSP contribution, and select your province/territory to calculate taxes.</p>

  
  <label for="income">年收入 (Annual Income):</label>
  <input type="number" id="income" step="0.01">
  <br>

  <label for="rrspContribution">退休储蓄计划存款 (RRSP Contribution):</label>
  <input type="number" id="rrspContribution" step="0.01">
  <br>

  <label for="province">选择您的省份 (Select Province/Territory):</label>
  <select id="province">
    <option value="Alberta">Alberta</option>
    <option value="British Columbia">British Columbia</option>
    <option value="Ontario">Ontario</option>
    <option value="Quebec">Quebec</option>
    <option value="Nova Scotia">Nova Scotia</option>
    <option value="Manitoba">Manitoba</option>
    <option value="New Brunswick">New Brunswick</option>
    <option value="Newfoundland and Labrador">Newfoundland and Labrador</option>
    <option value="Northwest Territories">Northwest Territories</option>
    <option value="Nunavut">Nunavut</option>
    <option value="Prince Edward Island">Prince Edward Island</option>
    <option value="Saskatchewan">Saskatchewan</option>
    <option value="Yukon">Yukon</option>
  </select>
  <br>

  <button onclick="calculateTax()">Calculate</button>
  <br>

  <div id="results" style="display: none;">
    <p>无 RRSP 捐款的总税额 (Total tax without RRSP contribution): $<span id="totalTaxWithoutRRSP">0.00</span></p>
    <p>有 RRSP 捐款的总税额 (Total tax with RRSP contribution): $<span id="totalTaxWithRRSP">0.00</span></p>
	<p>总税款节省金额 (Total tax savings): $<span id="rrspTaxSavings">0.00</span></p>
  </div>
</body>
</html>
