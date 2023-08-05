# Summary Data Preprocessing by DataLab

## Data Cleansing
### Handle Missing Values
Berdasarkan proses analisa, dapat disimpulkan bahwa tidak terdapat nilai kosong pada data employee attrition. Oleh karena itu, tidak dilakukan proses handling missing value.

### Handle Duplicated Data
Berdasarkan proses analisa, dapat disimpulkan bahwa tidak terdapat data yang terduplikasi, sehingga tidak diperlukan proses handling duplicated data.

### Handle Outliers
- Dilakukan proses penghapusan data outliers pada kolom MonthlyIncome, NumCompaniesWorked, TotalWorkingYears, TrainingTimesLastYear, YearsAtCompany, YearsInCurrentRole, YearsSinceLastPromotion, dan YearsWithCurrManager.
- Berdasarkan proses pada tahap ini, didapatkan bahwa sebelum dilakukan penghapusan data *outliers* terdapat **1470** baris data dan setelah dilakukan penghapusan data *outliers* terdapat **1387** baris data.

### Feature Encoding
Pada tahap ini dilakukan proses feature encoding pada tabel Attrition, BusinessTravel, Gender, dan OverTime menggunakan metode Label Encoder serta dilakukan proses feature encoding pada kolom Departemen, EducationField, Jobrole, MaritalStatus, dan Over18 menggunakan metode one-hot encoding.

## Feature Engineering
### Feature Selection
- Pada tahap ini, dipilih kolom Attrition sebagai kolom target.
- Dilakukan proses penghapusan pada kolom EmployeeCount karena hanya memiliki 1 nilai unik.
- Dilakukan proses penghapusan pada kolom EmployeeNumber, StandardHours, dan Over18 karena kolom tersebut memiliki jumlah nilai unik yang sama dengan jumlah baris pada data employee attrition.
- Dilakukan penghapusan pada kolom BusinessTravel, Departement, Education, EducationalField, Gender, HourlyRate, MaritalStatus, MonthlyRate, PercentSalaryHike, PerformanceRating, StandardHours, dan YearsSinceLastPromotion karena memiliki nilai corelasi dibawah 0,05 terhadap target (kolom Attrition).   
- Berdasarkan proses analisa menggunakan heatmap didapatkan bahwa terdapat multicollinearity (korelasi antara dua kolom di atas 0.7) anatara kolom JobLevel, MonthlyIncome dan TotalWorkingYears serta kolom YearsAtCompany, YearsInCurrentRole, dan YearsWithCurrManager sehingga dilakukan penghapusan kolom JobLevel, MonthlyIncome, YearsAtCompany, YearsWithCurrentManager.

### Feature Transformation
Pada tahap ini, dilakukan proses feature transformation menggunakan metode standarscaler.

### Handling Class Imbalace
- Berdasarkan proses analisa, dapat disimpulkan bahwa terdapat 1158 karyawan yang masih bertahan diperusahaan dan 229 karyawan tidak.
- Perbandingan antara jumlah karyawan yang masih bertahan dan tidak adalah sekitar 1:5.
- Dilakukan proses handling class imbalance menggunakan metode SMOTE.

## Fitur Tambahan
Beberapa fitur tambahan yang mungkin akan sangat membantu untuk meningkatkan performa model :
- **WorkingHours (Integer)**: Jumlah jam kerja karyawan dalam satu bulan.
    Berdasarkan UU Ketenagakerjaan, rata-rata jumlah jam kerja karyawan dalam 1 bulan adalah 173 jam.
    Tujuan penambahan fitur ini adalah untuk menganalisa batas maksimum durasi overtime yang menyebabkan seorang karyawan memilih untuk tidak bertahan di suatu perusahaan.

- **Absence (Integer)**: Jumlah hari karyawan tidak masuk kerja dalam 1 bulan.
    Karyawan yang ingin keluar dari perusahaan cenderung untuk lebih banyak absen dibandingkan yang tidak.

- **ManagerSatisfaction (Integer)**: Tingkat kepuasan karyawan terhadap direct manager.
    Semakin tinggi tingkat kepuasan seorang karyawan terhadap direct manager, maka semakin rendah juga kemungkinan mereka untuk keluar dari perusahaan.

- **EmployeeEngagement (Integer)**: Tingkat keterlibatan karyawan dengan *event* yang diadakan oleh perusahaan dan hubungan dengan karyawan lainnya.
    Semakin tinggi tingkat keterlibatan seorang karyawan, maka semakin rendah juga kemungkinan mereka untuk keluar dari perusahaan.