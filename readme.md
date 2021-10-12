# JuniorTechTitan_JC_DS_VL_01_FinalProject
## Anggota Proyek :
1. Simon Perdananta [Email](mailto:simonperdananta@gmail.com)
1. Nurdin Sulaeman [Email](mailto:nurdinsulaeman28@gmail.com)
1. Prana Pramudita Kusdiananggalih [Email](mailto:pranapramudita@gmail.com)

PT Titan Tech adalah sebuah perusahaan multi nasional yang memiliki cabang di beberapa nergara, sehingga perusahaan juga memiliki karyawan yang tergolong banyak. Proses evaluasi untuk menentukan karyawan yang layak untuk mendapat promosi tentu membutuhkan pengamatan yang tepat terhadap aspek-aspek yang menjadi kunci penilaian untuk memperoleh keputusan yang akurat. Dan tentunya jika hal ini dilakukan secara manual oleh tim HR akan cukup memakan waktu. Belum lagi penentuan karyawan layak promosi yang tidak tepat akan merugikan perusahaan di sisi operasional cost, dan menimbulkan kesenjangan yang tidak adil di antara karyawan

Sebagai tim Data Scientist, kita ditugaskan untuk membantu menganalisa dan membangun sebuah model yang mampu mendefinisikan dan mengklasifikasikan karyawan mana yang sekiranya tepat untuk dapat di promosikan berdasarkan pemilihan fitur yang tepat. Sehingga proses evaluasi untuk program promosi karyawan menjadi lebih cepat dan efisien tanpa mengurangi keakuratannya.

<p align="center">
<img src="https://st4.depositphotos.com/4230659/23629/v/600/depositphotos_236292080-stock-illustration-isometric-robot-analyzes-the-database.jpg"/>
</p>

## Problems
1. Perusahaan membutuhkan bantuan agar proses evaluasi untuk menentukan karyawan mana yang layak promosi menjadi lebih cepat
1. Bagaimana menciptakan sistem klasifikasi yang akurat terhadap karyawan untuk menentukan mana karyawan layak promosi dan tidak

## Goals
1. Membuat model Machine Learning untuk membantu pemilihan karyawan yang layak promosi secara efisien
1. Membuat model klasifikasi yang akurat untuk mencegah kerugian perusahaan dari sisi operational cost

## Dataset 
**Dataset:** HR Analytics: Employee Promotion Data | **Source:** [Kaggle](https://www.kaggle.com/arashnic/hr-ana)

| No | Column | Description |
| -- | ------ | ----------- |
| 1 | item_id | ID unik karyawan |
| 2 | department | Departemen atau divisi karyawan |
| 3 | region | Wilayah kerja karyawan |
| 4 | education | Pendidikan terakhir karyawan |
| 5 | gender | Jenis kelamin karyawan |
| 6 | recruitment_channel | Saluran rekrutmen karyawan |
| 7 | no_of_trainings | Jumlah pelatihan yang diselesaikan pada tahun sebelumnya seperti pelatihan soft skill, keterampilan teknis, dll. |
| 8 | age | Umur karyawan |
| 9 | previous_year_rating | Rating karyawan pada tahun sebelumnya  |
| 10 | length_of_service | Lama karyawan bekerja (dalam tahun) |
| 11 | awards_won | Jika memenangkan penghargaan tahun lalu maka 1, jika tidak maka 0 |
| 12 | avg_training_score | Skor rata-rata dalam evaluasi pelatihan |
| 13 | is_promoted | Jika direkomendasikan promosi maka 1, jika tidak maka 0 |

## Steps
1. [Explore Data Analysis (EDA)](https://github.com/PurwadhikaDev/JuniorTechTitan_JC_DS_VL_01_FinalProject/blob/master/FINAL%20PROJECT%20-%20Explore%20Data%20Analysis.ipynb)
2. [Data Cleansing & Preparation](https://github.com/PurwadhikaDev/JuniorTechTitan_JC_DS_VL_01_FinalProject/blob/master/FINAL%20PROJECT%20-%20Data_Cleansing___Preparation.ipynb)
3. [Modeling & Evalulation](https://github.com/PurwadhikaDev/JuniorTechTitan_JC_DS_VL_01_FinalProject/blob/master/FINAL%20PROJECT%20-%20ML%20Modeling%2C%20Evaluation.ipynb)

## Summary EDA
-	Dari 54808 data karyawan,hanya  terdapat 4668 karyawan atau 8.52% dari keseluruhan karyawan yang mendapatkan kesempatan promosi
-	Dari hasil analisa yang telah dilakukan, kondisi perusahaan saat ini dalam mengklasifikasikan karyawan mana yang layak di promosikan, yaitu berdasarkan kinerja karyawan di tahun sebelumnya, misalnya seperti apakah karyawan tersebut pernah mendapatkan awards di tahun sebelumnya, rating atau peniliaian kinerja karyawan di tahun sebelumnya dan juga rata-rata nilai yang tinggi dari hasil training yang telah karyawan ikuti.
- No of Trainings atau jumlah training yang pernah di ikuti oleh seorang karyawan banyaknya hanya dilakukan satu kali oleh setiap karyawan. Karyawan yang mendapatkan training lebih dari satu kali atau bahkan hingga training lebih dari lima kali justru kesempatan untuk mendapatkan promosinya semakin menurun jika di bandingkan dengan karyawan yang hanya melakukan satu kali training saja.
- Umur dan lama kerja seorang karyawan tentu saja memiliki korelasi yang positif, namun jika dilihat secara statistik lama kerja seorang karyawan tidak memiliki pengaruh yang signifikan terhadap promosi, begitu juga dengan umur seorang karyawan. Karyawan dengan rentang umur 26 hingga 40 tahun memiliki kesempatan sedikit lebih besar untuk mendapatkan promosi jika di bandingkan dengan umur diatas atau dibawahnya. 
- Seperti yang telah kita ketahui data ini digunakan untuk mengklasifikasikan karyawan yang layak promosi namun hanya untuk posisi manager kebawah. Jadi walaupun lama kerja seorang karyawan tidak memiliki pengaruh positif terhadap promosi, bisadi asumsikan bahwa karyawan yang memiliki lama kerja cukup tinggi atau lebih dari 20 tahun kerja kemungkinan memiliki jabatan atau posisi diatas manager.
- Awards, Previous Year Rating dan Average Training score adalah tiga feature yang paling berpengaruh dalam peluang atau kesempatan karyawan untuk mendapatkan promosi. Seorang karyawan yang memiliki rating di angka 5 berpeluang 16.36% untuk promosi. Seorang karyawan yang pernah mendapatkan awards memiliki peluang 44.02% untuk di promosikan. Karyawan dengan Avg Training Score 90-100 memiliki peluang 76.83% untuk di promosikan, bahkan untuk Avg Training Score >95 dia memiliki peluang 100% atau pasti akan di promosikan.
- Tingkat pendidikan karyawan di perusahaan di dominasi oleh karyawan dengan tingkat pendidikan Bachelor’s. Namun jika dibandngkan dengan masing-masing tingkat pendidikan yang ada, kesempatan untuk mendapatkan promosi di tingkat pendidikannya masing-masing memiliki persentase yang tidak jauh berbeda signifikan, karena mungkin promosi yang dilakukan menyesuaikan dengan divisi dan backround dari pendidikannya masing-masing.
- Walaupun perusahaan memiliki karyawan laki-laki yang lebih banyak dari perempuan, namun baik laki-laki atau perempuan memiliki kesempatan yang sama untuk di promosikan.
- Karyawan dengan proses perekrutan berdasarkan referensi memiliki kesempatan di promosikan sedikit lebih tinggi dibandingkan dengan karyawan yang berasal dari outsorcing atau yang lainnya.

## References
1. https://towardsdatascience.com/building-a-logistic-regression-in-python-step-by-step-becd4d56c9c8