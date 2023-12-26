```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Account Tables</title>
    <style>
      .accounts-table {
        width: 100%;
        border-collapse: collapse;
        margin-bottom: 20px; /* Adjust as needed */
      }

      /* Border styling for th elements, assuming you want no borders on these */
      .accounts-table th {
        padding: 8px; /* Adjust padding as needed */
        text-align: left;
        background-color: #ccc; /* Light grey background for header cells */
        color: black;
        border: none;
      }

      /* Internal borders for td elements, no borders for the outer edges */
      .accounts-table td {
        padding: 8px;
        text-align: left;
        border-right: 1px solid #ddd;
        border-bottom: 1px solid #ddd;
      }
      td[colspan] {
        background-color: #f2f2f2; /* Your desired background color */
      }
      /* First td of each row: no left border */
      .accounts-table tbody tr td:first-child {
        border-left: none;
      }

      /* First row of tbody: top border only */
      .accounts-table tbody tr:first-child td {
        border-top: 1px solid #ddd; /* Top border for the first row of tbody */
      }

      /* Last td of each row: no right border */
      .accounts-table tbody tr td:last-child {
        border-right: none;
      }

      /* Last row of tbody: no bottom border */
      .accounts-table tbody tr:last-child td {
        border-bottom: none;
      }

      /* Additional CSS here for zebra striping, subtotal row background, etc. */
    </style>
  </head>
  <body>
    <table class="accounts-table">
      <thead>
        <tr>
          <th>Account title</th>
          <th>Account number</th>
          <th>Current available</th>
          <th>Current ledger</th>
          <th>As at date / time</th>
        </tr>
      </thead>
      <tbody>
        <tr class="subtotal">
          <td colspan="100%">BHD (Bahraini Dinar)</td>
        </tr>
        <!-- Account rows -->
        <tr>
          <td>AIP Centigen</td>
          <td>001-000187-203</td>
          <td>59,128.05</td>
          <td>76,879.01</td>
          <td>31 Jan 2017 00:00</td>
        </tr>
        <!-- Account rows -->
        <tr>
          <td>AIP Centigen</td>
          <td>001-000187-203</td>
          <td>59,128.05</td>
          <td>76,879.01</td>
          <td>31 Jan 2017 00:00</td>
        </tr>
        <tr class="subtotal">
          <td colspan="100%">BHD (Bahraini Dinar)</td>
        </tr>
        <!-- Repeat rows for each account -->
        <!-- Subtotal row -->
        <tr class="subtotal">
          <td>Subtotal</td>
          <td></td>
          <td>96,229.52</td>
          <td>40,661.94</td>
          <td></td>
        </tr>
        <!-- Repeat the pattern for other currencies -->
      </tbody>
    </table>

    <!-- Repeat the whole <table> block for other currencies with similar structure -->
  </body>
</html>
```
