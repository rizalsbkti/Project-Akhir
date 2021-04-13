# Project-Akhir

LATAR BELAKANG
  Seorang manajer di bank merasa terganggu dengan semakin banyaknya pelanggan yang meninggalkan layanan kartu kredit mereka. Pihak bank akan sangat menghargai jika
seseorang dapat memprediksi untuk pelanggan yang akan berhenti menggunakan jasa yang ditawarkan, sehingga pihak bank dapat secara proaktif pergi ke pelanggan untuk
memberikan mereka layanan yang lebih baik dan mengubah keputusan pelanggan ke arah yang berlawanan.
  Sekarang, kumpulan data ini terdiri dari 10.000 pelanggan yang menyebutkan usia, gaji, status_kawinan, batas kartu kredit, kategori kartu kredit, dll. Ada hampir 20 fitur.
  Pihak Bank hanya memiliki 16,07% pelanggan yang berhenti menggunakan jasa kartu kridit. Karena itu, tidak mudah melatih model kami untuk memprediksi pelanggan yang berhenti.

RUMUSAN MASALAH
Bagaimana memprediksi seorang nasabah akan berhenti atau tidak dalam penggunaan kartu kredit?

TUJUAN
Memprediksi seorang nasabah akan berhenti atau tidak dalam penggunaan kartu kredit.

MANFAAT
Dapat menekan kerugian akibat penurunan pengguna layanan kartu kredit.

EDA SUMMARY

CATEGORICAL DATA
1. Pada feature Categorical, Attrition Customer secara signifikan lebih rendah daripada Existing Customer.
2. Angka Attrition tertinggi dari masing-masing feature:
    * Gender:
            - Jumlah pelanggan dengan Attrition tertinggi pada Feature Gender adalah female dengan persentase lebih besar 2,3%. Rasio Gender Femalejuga lebih besar dibandingkan Existing, dengan nilai 0.17. Angka ini lebih besar dibandingkan Gender Male untuk Attrition dengan nilai 0.14. Namun angka ini tidak 
    * Education Level:
            - Jumlah pelanggan dengan Attrition tertinggi pada Feature Education Level adalah Graduate dengan persentase 4.81%. Untuk Education Level, rasio pelanggan yang Attrition kurang lebih sama dari tingkat High School hingga Collage. Dan, perlahan-lahan terjadi penaikan rasio dari tingkat pascasarjana ke doktoral.
            - Peningkatan rasio ini dikarenakan jumlahnya makin sedikit ketika Educational Levelnya meningkat, jadi tidak bisa dikatakan rasio yang tinggi memiliki kecenderungan untuk Attrition lebih besar, perlu dilihat juga dari aspek lainnya.

    * Marital Status
            - Jumlah pelanggan dengan Attrition tertinggi pada Feature Marital Status adalah Married dengan persentase 7% dan Single sebesar 6.6%. Rasio pada Single 0.16, Divorce dan Unknown sebesar 0.17. Angka rasio pada Single, Divorce, dan Unknown lebih besar dibandingkan dengan Married dengan nilai 0.15.
            - Jadi, kategori Single lebih besar chance untuk Attrition, dikarenakan rasio yang lebih besar dibandingkan dengan Married dan dengan jumlah yang tidak jauh berbeda dibandingkan Married.
            - Kecenderungan untuk Attrition pada Marital Status Single bisa dipicu dikarenakan belum memiliki jumlah tanggungan yang lebih banyak dibandingkan yang Married dan Divorced.

    * Income Category
            - Jumlah pelanggan dengan Attrition tertinggi pada Feature Income Category adalah Less than 40k dengan persentase 6.04%. Semakin tinggi Income Categorynya, semakin turun jumlah pelanggannya.
            - Rasio Attrition terendah pada Income Category 60k-80k dengan nilai 0.18 dibandingkan dengan kategori lainnya.
            - Rasio Income Category 120k+ sama dengan Less than 40k dengan nilai 0.17, rasio ini tertinggi dibandingkan dengan kategori lainnya. Rasio pada 120k+ tinggi karena tingkat penghasilan paling tinggi dan jumlahnya paling sedikit, oleh karena itu rasio attritionnya tinggi walaupun jumlah pelanggan yang attrition berbeda 4.8% dibandingkan Less than 40k.
        
    * Card Category
            - Jumlah pelanggan dengan Attrition tertinggi pada feature Card Category adalah Blue, dengan persentase sangat besar yaitu 15%, angka ini mendekati total dari Attrition Customer sebesar 16.07%.
            - Bisa dikatakan juga mayoritas Attrition Customer pada Card Category Blue.

NUMERICAL DATA
1. Total Revolving Balance
    - Selisih antara Credit Limit dengan Average Open to Buy. Artinya sisa hutang dari peminjaman yang belum terbayarkan tiap bulannya, dalam 12 bulan dengan rata-rata perbulannya kurang dari 750 lebih cenderung untuk Attrition.
    - Hipotesa saya, para pengguna yang Revolving Balance kecil tiap bulannya tidak memiliki kecenderungan menggunakan sesuai dengan porsinya. Pengguna dengan tingkat pendapatannya sesuai dengan kebutuhannya sehari-hari. Jadi, pengguna dengan pendapatan yang stabil seperti ini merasa dirugikan dengan penggunaan kartu kredit yang ada bunganya, sehingga mereka cenderung untuk berhenti atau pindah ke bank lain dengan bunga yang lebih rendah.

2. Total Transaction Amount
    - Attrition Customer tinggi pada jumlah transaksi kurang dari 2500 dolar tiap customer rata-rata dalam 12 bulan terakhir. Customer ini merasa jarang menggunakan kartu kredit yang membuat mereka cenderung berhenti.

3. Total_Trans_Ct
    - Attrition Customer tinggi pada jumlah transaksi kurang dari 50 kali tiap customer dalam 12 bulan terakhir. Customer ini merasa jarang menggunakan kartu kredit yang membuat mereka cenderung berhenti.
    
4. Change in Transaction Count (Q4 over Q1)
    - Change in Transaction Count merupakan rasio kenaikan penggunaan jumlah kartu kredit perbandingan tiap quarternya, Customer Attrition tertinggi dengan nilai kurang dari 0,5. Hal ini berarti menandakan tidak ada perubahan jumlah penggunaan kartu kredit tidak quarternya.

5. Average Utilization Ratio
    - Feature ini menjelaskan rasio seberapa berguna pemanfaatan kartu kredit bagi customernya. Rasio yang Attrition tertinggi adalah pada kurang dari 0.05. Dapat dilhat berarti penggunaan yang rendah dari customer dapat memicu Attrition.


**General Summary and What Solution that I can Help**

Dari analisa yang saya lakukan, dapat disimpulkan bahwa mayoritas pengguna dan mayoritas Attrition pada:
1.	Tingkat pendidikan dari SMA sampai S1.
2.	Marital Status menikah dan Single.
3.	Income Catogry Less Than 40 dolar.
4.	Card Category Blue.
5.	Usia tertinggi dari range 37 sampai 59 tahun.
6.	Jumlah tanggungan 2 dan 3.
7.	Penggunaan kartu tertinggi selama 36 bulan.
8.	Customer tertinggi menggunakan produk berjumlah 3.
9.	Customer tidak aktif menggunakan kartu paling lama 3 bulan.
10.	Dan kurangnya rasio penggunaan kartu dalam kegiatan sehari-hari.

Dari permasalahan yang ada, dapat kita ambil solusinya untuk menekan angka Attrion Customer:
1.	Perluas penggunaan kartu kredit khususnya untuk kartu Category Blue dari berbagai sector lebih luas lagi, market place, berbagai merchant, property,
kesehatan, pendidikan, transportasi dan lain-lain. Buat promosi yang dapat menimbulkan ketertarikan untuk menggunakan kartu kredit. Dengan cara seperti ini
otomatis rasio penggunaan kartu kredit dan membuat customer berpikir kembali bila berhenti menggunakannya.

2.	Buat persyaratan apabila kartu tidak digunakan sama sekali dalam 2 bulan, akan dikenakan biaya administrasi.

3.	Buat persyaratan kembali apabila sudah berlangganan kartu kredit dan apabila nanti berhenti, maka promo-promo yang didapat pelanggan lama tidak akan berlaku kembali ketika mendaftar kembali.




MACHINE LEARNING
PRE POCESSING
Terdapatoutliers pada feature:
    1. Credit_Limit
    2. Avg_Open_To_Buy
    3. Total_Amt_Chng_Q4_Q1
    4. Total_Trans_Amt
    5. Total_Ct_Chng_Q4_Q1
    6. Customer_Age
    7. Months_Inactive_12_mon
    8. Contacts_Count_12_mon
    9. Total_Trans_Ct
    
    Preprocessing Scheme
- OneHot: Gender, Education_Level, Marital_Status, Income_Category, Card_Category
- Min Max Scaller: Customer_Age, Credit_Limit, Avg_Open_To_Buy, Total_Amt_Chng_Q4_Q1, Total_Trans_Amt, Total_Ct_Chng_Q4_Q1, Months_Inactive_12_mon, Contacts_Count_12_mon.
- Passthrogh: Dependent_count, Months_on_book, Total_Relationship_Count, Total_Revolving_Bal, Total_Trans_Ct, Total_Trans_Ct, Avg_Utilization_Ratio

Existing Customer    83.934038
Attrited Customer    16.065962
Indicated Imbalance Data

* Attrited Customers = 1
* Existing Customers = 0

* *0 = Keep Use*
* *1 = Off*

        - TN: Ada pelanggan yang diprediksi dengan Keep Use dan kenyataannya Off
        - TP: Ada pelanggan yang diprediksi dengan Off dan kenyataannya Off Off
        - FP: Ada pelanggan yang diprediksi dengan Off, padahal Keep Use
        - FN: Ada pelanggan yang diprediksi dengan Keep Use padahal Off

Tindakan:
* FP: Salah prediksi, tidak berpengaruh apa apa
* FN: Perusahaan rugi karena kehilangan pelanggan

- > Yang akan di tekan adalah FN, recall

Membuat Transformer
transformer= ColumnTransformer([
    ('one_hot',OneHotEncoder(drop='first'),['Gender','Education_Level','Marital_Status','Income_Category','Card_Category']),
    ('scale',MinMaxScaler(), ['Credit_Limit', 'Avg_Open_To_Buy', 'Total_Amt_Chng_Q4_Q1', 'Total_Trans_Amt', 'Total_Ct_Chng_Q4_Q1', 'Customer_Age', 'Months_Inactive_12_mon', 'Contacts_Count_12_mon','Total_Trans_Ct'])]
    , remainder='passthrough')

*Splitting Data*

*Define Model*
- I use 4 models to predict:
    * Logistic Regression
    * Decision Tree Classifier
    * K-Nearest Neighbor
    * Random Forest
    
*Cross Validation*
  method	                 mean score	std score	recall score
0	Logistic Regression	      0.493465	0.036344	0.514344
1	Decision Tree Classifier	0.781436	0.034123	0.805328
2	KNN Classifier	          0.192279	0.031094	0.206967
3	Random Forest Classifier	0.759456	0.025778	0.782787

Decission Tree dan Random Forest tertinggi.

*HANDLING IMBALANCE*
*Random Over Sampling*
 	method	                            mean score	std score	recall score
0	Logistic Regression OverSampling	    0.841070	0.020810	0.840164
1	Decision Tree Classifier OverSampling	0.776126	0.020495	0.750000
2	KNN Classifier OverSampling	          0.367872	0.043233	0.368852
3	Random Forest Classifier OverSampling	0.818294	0.022085	0.834016
    
*Random Under Sampling*
	method	                                mean score	std score	recall score
0	Logistic Regression UnderSampling	      0.828770	0.023609	0.834016
1	Decision Tree Classifier UnderSampling	0.886765	0.014910	0.891393
2	KNN Classifier UnderSampling	          0.503091	0.046995	0.520492
3	Random Forest Classifier UnderSampling	0.941186	0.008080	0.942623

Recall Score Random Forest Classifier UnderSampling naik menjadi 0.942623 dari sebelumnya 0.782787.

*Hyper Paramether Tunning*
estimator = Pipeline([
    ('transformer', transformer),
    ('balancing', rus),
    ('model', rf)
])

hyperparam_space={
    'model__max_depth':[2,5,7,10],
    'model__min_samples_leaf':[1,5,10,20,50,100],
    'model__min_samples_split':[1,5,10,20,50,100],
    'model__criterion':['gini','entropy']
}


skfold=StratifiedKFold(n_splits=5)

grid_search=GridSearchCV(
    estimator,
    param_grid=hyperparam_space,
    cv=skfold,
    scoring='recall',
    n_jobs=-1
)


print('best score', grid_search.best_score_)
print('best param', grid_search.best_params_)

best score 0.9429438132776877
best param {'model__criterion': 'gini', 'model__max_depth': 10, 'model__min_samples_leaf': 1, 'model__min_samples_split': 10}

grid_search.best_estimator_.fit(X_train, y_train)
y_predict = grid_search.best_estimator_.predict(X_test)
recall_score(y_test, y_predict)

0.944672131147541, Recall Score Naik.


*Saving Model with Pickle*
grid_search.best_estimator_.fit(X, y)

Pipeline(steps=[('transformer',
                 ColumnTransformer(remainder='passthrough',
                                   transformers=[('one_hot',
                                                  OneHotEncoder(drop='first'),
                                                  ['Gender', 'Education_Level',
                                                   'Marital_Status',
                                                   'Income_Category',
                                                   'Card_Category']),
                                                 ('scale', MinMaxScaler(),
                                                  ['Credit_Limit',
                                                   'Avg_Open_To_Buy',
                                                   'Total_Amt_Chng_Q4_Q1',
                                                   'Total_Trans_Amt',
                                                   'Total_Ct_Chng_Q4_Q1',
                                                   'Customer_Age',
                                                   'Months_Inactive_12_mon',
                                                   'Contacts_Count_12_mon',
                                                   'Total_Trans_Ct'])])),
                ('balancing', RandomUnderSampler(random_state=1010)),
                ('model',
                 RandomForestClassifier(max_depth=10, min_samples_split=10,
                                        random_state=1010))])

file_name = 'Attrition_Bank.sav'

pickle.dump(grid_search.best_estimator_, open(file_name,'wb'))

loaded_model = pickle.load(open(file_name,'rb'))
loaded_model.predict(X_test)

att_pred = pd.DataFrame({
    'Customer_Age': [48],
    'Gender': ['M'],
    'Dependent_count': [2],
    'Education_Level': ['Graduate'],
    'Marital_Status': ['Married'],
    'Income_Category': ['$60K - $80K'],
    'Card_Category': ['Silver'],
    'Months_on_book': [35],
    'Total_Relationship_Count': [2],
    'Months_Inactive_12_mon': [4],
    'Contacts_Count_12_mon': [4],
    'Credit_Limit':[34516],
    'Total_Revolving_Bal':[0],
    'Avg_Open_To_Buy': [34516],
    'Total_Amt_Chng_Q4_Q1': [0.763],
    'Total_Trans_Amt':[691],
    'Total_Trans_Ct': [15],
    'Total_Ct_Chng_Q4_Q1': [0.5],
    'Avg_Utilization_Ratio': [0.0]
})

loaded_model.predict(att_pred)
array([1])
loaded_model.predict_proba(att_pred)
array([[0.05291321, 0.94708679]])
