# -Importing-Exporting-Data-in-R
In this respository I will explain what I learned the topics about importing and exporting Data in R.
1️⃣ CSV Files
✅ Import CSV
# Import CSV file
data <- read.csv("data.csv")

# View first rows
head(data)

✅ Export CSV
# Export to CSV file
write.csv(data, "output.csv", row.names = FALSE)

2️⃣ Excel Files

🔹 To work with Excel, we usually need the readxl and writexl packages.

✅ Import Excel
# Install once
install.packages("readxl")

# Load
library(readxl)

# Import Excel file
data <- read_excel("data.xlsx")

✅ Export Excel
# Install once
install.packages("writexl")

library(writexl)

# Export data frame to Excel
write_xlsx(data, "output.xlsx")

3️⃣ Text Files (TXT)
✅ Import TXT
# Import tab-delimited text file
data <- read.table("data.txt", header = TRUE, sep = "\t")

# Or space-delimited
data <- read.table("data.txt", header = TRUE)

✅ Export TXT
write.table(data, "output.txt", sep = "\t", row.names = FALSE)


📌 Summary:

CSV → read.csv() / write.csv()

Excel → read_excel() / write_xlsx() (need packages)

Text → read.table() / write.table()

✨ Pro tip: Always check your working directory with:

getwd()   # see current folder
setwd("C:/path/to/folder")  # set folder

