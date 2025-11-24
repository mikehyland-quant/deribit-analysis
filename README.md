# Deribit.xlsx and Methods_xlWings
The code below will output most of the data to the excel spreadsheet via xlWings and the shortcuts contained in the .py file.

# Deribit_Get_Data
This code makes contact with the Deribit platform and extracts information and market pricing for Bitcoin futures and options.

# Deribit_Confirm_Greeks and Deribit_Confirm_Vols
This code uses the data gathered above and the code in the Options_Math repository to compute greeks and vols that are then compared to the Deribit outputs as an accuracy check.

# Deribit_Enrich
This code improves the market bids and asks from above by applying arbitrage free pricing rules.  More information about this process is described in comments in the code.

# Deribit_SABR_Calibrate and Deribit_Wow_Alpha_Calibrate
This code solves for parameters to describe Deribit_Enrich skew via SABR and Wow-Alpha.  The Wow-Alpha parameterization usually fits Bitcoin data very well.  Further, the Wow-Alpha parameters themselves are easy to convert to functions based on time to expiry.

# Deribit_Daily_Vol_Calculator
This code will solve for forward volatilities across time slices (usually days) such that the sum of the time slice vols equal the term vols of listed options.  This allows for calibrating of OTC option vols in a consistent manner with listed option vols.
