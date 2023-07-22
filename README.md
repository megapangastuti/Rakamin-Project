# Summary Insight

## Problem Statement
Diketahui sebanyak **16.1%** karyawan memutuskan untuk **meninggalkan perusahaan**. Hal tersebut cukup berpengaruh terhadap kinerja perusahaan. Oleh karena itu, perlu dilakukan proses analisa mengenai **faktor-faktor** apa saja yang menyebabkan atau menjadi alasan seorang karyawan memilih untuk meninggalkan perusahaan, sehingga team HR dapat memberikan *treatment* khusus kepada karyawan agar tidak meninggalkan perusahaan.

Selain itu, setelah mengetahui faktor-faktor apa saja yang menyebabkan seorang karyawan memilih untuk meninggalkan perusahaan, team HR juga dapat menjadikan hal tersebut sebagai **acuan** untuk menyaring **karyawan baru** yang memiliki potensi yang lebih rendah untuk meninggalkan perusahaan.

## Goals:
- Mengurangi tingkat employee attrition (resign) untuk pekerja yang berada di perusahaan.
- Mencegah kemungkinan untuk karyawan baru yang berpotensi untuk employee attrition (resign) di kemudian hari dengan mengetahui faktor-faktor yang dapat menyebabkan seorang karyawan resign.

## Objectives:
- Menganalisa faktor-faktor dari data yang dimiliki terhadap potensi employee attrition (resign).
- Membuat model yang dapat digunakan untuk memprediksi karyawan-karyawan yang berpotensi untuk meninggalkan perusahaan.

## Business Metrics
Employee attrition rate (%) atau jumlah pegawai yang meninggalkan perusahaan.

## Insight 
Kemudian, akan dilakukan proses analisa lebih lanjut terhadap data
employee attrition dengan menggunakan framework **5W + 1H** :

- **What**    : Apa yang membuat karyawan meninggalkan perusahaan? <br> Akan dilakukan proses analisa berdasarkan data pada kolom `OverTime`, `JobInvolvement`, `BusinessTravel` <br>
- **Who**		  : Siapa saja karyawan yang meninggalkan perusahaan? <br>  Akan dilakukan proses analisa berdasarkan data pada kolom `Age`, `Gender`, `JobRole`, `JobLevel`, `MaritalStatus`, `Education`, `EducationField`
- **Why**  	  : Alasan apa yang membuat karyawan yang meninggalkan perusahaan? <br>
Akan dilakukan proses analisa berdasarkan data pada kolom `MonthlyIncome`, `EnvironmentSatisfaction`, `JobSatisfaction` <br>
- **Where**	  : Dari mana sajakah karyawan yang meninggalkan perusahaan? <br>
Akan dilakukan proses analisa berdasarkan data pada kolom `Department` <br>
- **When** 	  : Kapan biasanya karyawan meninggalkan perusahaan?<br>
Akan dilakukan proses analisa berdasarkan data pada kolom `TotalWorkingYears`, `YearsAtCompany`, `YearsInCurrentRole`, `YearsWithCurrManager`

### What: Apa yang membuat karyawan meninggalkan perusahaan?
1. Karyawan yang bekerja melebihi jam kerja reguler (over time) memiliki Attrition Rate yang lebih tinggi dibandingkan dengan karyawan yang tidak bekerja lembur.
2. Karyawan yang memiliki keterlibatan kerja yang lebih rendah memiliki Attrition Rate yang lebih tinggi.
3. Karyawan yang lebih sering melakukan business travel memiliki Attrition Rate yang lebih tinggi.

### Who: Siapa saja karyawan yang meninggalkan perusahaan?
Berdasarkan grafik di atas dapat disimpulkan bahwa :
1. Karyawan dengan rentang umur di bawah 40 tahun cenderung memiliki attrition rate yang lebih tinggi. Kemudian, karyawan dengan rentang umur sekitar 25 - 35 tahun memiliki attrition rate yang paling tinggi.
2. Karyawan pria cenderung memiliki attrition rate yang hampir sama dengan karyawan wanita.
3. Karyawan yang memiliki Job Level yang lebih rendah memiliki attrition rate yang lebih tinggi. Kemudian, karyawan yang memiliki Job Level 1 merupakan tipe karyawan dengan attrition rate paling tinggi.
4. Karyawan dengan marital status belum menikah (single) cenderung memiliki attrition rate yang lebih tinggi dibandingkan karyawan  yang sudah menikah dan yang berstatus sudah bercerai. Selain itu, karyawan dengan marital status divorced memiliki attrition rate paling rendah atau merupakan tipe karyawan yang paling banyak bertahan di perusahaan.
5. Karyawan yang memiliki educational level yang lebih rendah cenderung memiliki attrition rate yang lebih tinggi. Kemudian, karyawan dengan yang memiliki educational level 1 merupakan tipe karyawan yang memiliki attrition rate paling tinggi.
6. Karyawan yang memiliki latar belakang pendidikan di bidang Human Resources, Technical Degree, dan Marketing merupakan 3 golongan karyawan yang memiliki attrition rate paling tinggi.
7. Karyawan yang menjabat sebagai Sales Representative, Laboratory Technician, dan Human Resources merupakan 3 golongan karyawan yang memiliki attrition rate paling tinggi.


### Why: Alasan apa yang membuat karyawan yang meninggalkan perusahaan?
1. Karyawan dengan Monthly Income sekitar 1800 - 3200 merupakan tipe karyawan yang memiliki Attrition Rate yang paling tinggi. Kemudian karyawan dengan Monthly Income sekitar 13000 - 19000 merupakan tipe karyawan yang memiliki Attrition Rate yang paling rendah.
2. Karyawan yang memiliki jabatan sebagai Manager memiliki Monthly Income paling tinggi sedangkan karyawan dengan jabatan sebagai Sales Representative memiliki Monthly Income paling rendah.
3. Karyawan yang memiliki tingkat Environment Satisfaction yang lebih rendah cenderung memiliki Attrition Rate yang lebih tinggi. Kemudian, didapatkan bahwa karyawan yang memiliki Environment Satisfaction bernilai 1 merupakan tipe karyawan yang memiliki Attrition Rate yang paling tinggi.
4. Karyawan yang memiliki tingkat Job Satisfaction yang lebih rendah cenderung memiliki Attrition Rate yang lebih tinggi. Kemudian, didapatkan bahwa karyawan yang memiliki Job Satisfaction bernilai 1 merupakan tipe karyawan yang memiliki Attrition Rate yang paling tinggi.

### Where: Dari mana sajakah karyawan yang meninggalkan perusahaan?
Karyawan yang bekerja pada Departemen Sales memiliki Attrition Rate yang paling tinggi dibandingkan dengan departemen lainnya.

### When: Kapan biasanya karyawan meninggalkan perusahaan?
1. Karyawan dengan Total Working Years sekitar 0 - 2 tahun serta 4,5 - 6 tahun merupakan dua tipe karyawan yang memiliki Attrition Rate yang paling tinggi.
2. Karyawan dengan nilai Years at Company sekitar 0 - 1 tahun tipe karyawan yang memiliki Attrition Rate yang paling tinggi.
3. Karyawan dengan nilai Years in Current Role sekitar 0 - 1 tahun serta 1,75 - 2,6 tahun merupakan dua tipe karyawan yang memiliki Attrition Rate yang paling tinggi



