SQL MODULS
SQL - on postgresql
#postgresql
This is how I learn SQL
Hello My name is Sinan. My main purpose on this project is to show what sort of technical skills I know on SQL as well as my knowlodge on Structured query language.

**1.SQL DATA TYPES**

**Metinsel (String) Veri Tipleri**

-_CHAR_: Sabit uzunluktaki metin verilerini tanımlamak için kullanılır. Örnek kullanım; CHAR(20) şeklindedir. Burada giriş yapılacak metin uzunluğu
en fazla 20 karakter olabilir. Eğer metin 20 karakterden daha uzunsa geri kalan kısım atlanır. Eğer metin 20 karakterden kısaysa kalan kısımlar boşlukla
doldurulur.

-_VARCHAR_: Değişken uzunluktaki metin verilerini tanımlamak için kullanılır. Örnek kullanım VARCHAR(255) şeklindedir. 255 karakter uzunluğunda bir metin 
alanı oluşturulur. Eğer giriş verisi 20 karakter uzunluğundaysa yalnızca 20 karakterlik alan tutulur. 

-_TEXT_: Uzun metin verileri için kullanılır. CHAR ve VARCHAR'a göre daha uzun karakterdeki metin verilerini saklar. Bir makale veya bildiri içeriği TEXT
karakteri olarak tanımlanabilir. Max. 2^32-1 (4GB) veri saklayabilir. 

**Sayısal (Numeric) Veri Tipleri**

-_INTEGER(INT)_: Bir kişinin yaşı, ürün adet sayısı gibi tam sayıları tanımlamak için kullanılır. Genellikle 4 byte'lık bir veri tipidir. -2^31 
ile 2^31-1 arasında bir sayı saklayabilir.

-_SMALLINT_: Küçük tam sayılar için kullanılır. bir ürünün stok miktarını saklamak için SMALLINT kullanılabilir. genellikle 2 byte'lık bir veri tipidir ve
-2^15 ile  2^15-1 arasında bir sayı saklayabilir.

-_BIGINT_: Büyük tam sayılar için kullanılır. Örneğin, bir ülkenin nüfusunu saklamak için BIGINT kullanılabilir. BIGINT veri tipi genellikle 8 byte'lık bir veri 
tipidir ve -2^63 ile 2^63-1 arasında bir sayı saklayabilir.

-_FLOAT_: Ondalıklı sayılar için kullanılır. Örneğin, bir ürünün fiyatını saklamak için FLOAT kullanılabilir. FLOAT veri tipi genellikle 4 byte'lık bir veri tipidir 
ve ondalık noktasına kadar 7 veya 8 hane hassasiyette bir sayı saklayabilir.

-_DECIMAL_: Ondalıklı sayıları sabit bir hassasiyette saklar. Örneğin, DECIMAL(10,2) veri tipi, en fazla 10 rakamlı ve 2 ondalıklı sayıları saklar. Bu veri tipi, 
hassasiyet ve doğruluğu ön planda tutan uygulamalar için idealdir. Finansal hesaplamalar için DECIMAL(10,4) veri tipini kullanabilirsiniz.

-_DOUBLE PRECISION_:Ondalıklı sayıları daha yüksek bir hassasiyette saklar. Bu veri tipi, daha büyük sayıları ve daha yüksek hassasiyeti gerektiren uygulamalar için idealdir. 
Bir fiziksel ölçüm için DOUBLE PRECISION kullanabilirsiniz.


**BOOLEAN Veri Tipi**

_BOOLEAN_ veri tipi, true/false (doğru/yanlış) değerlerini saklamak için kullanılır. Bu veri tipi, sadece iki değer alabilir: true ve false. Örnek verecek olursak:

Bir kullanıcının hesabının aktif/deaktif durumunu saklamak için BOOLEAN veri tipi kullanabilirsiniz.
Bir ürünün stokta/stokta olmadığı durumunu saklamak için BOOLEAN veri tipi kullanabilirsiniz.
Bir sorunun çözüldü/çözülmedi durumunu saklamak için BOOLEAN veri tipi kullanabilirsiniz.


**Tarih-Zaman Veri Tipleri**

-_DATE_: Sadece tarih bilgisini saklar, "2022-12-31" gibi. Örneğin bir ürünün son kullanma tarihini saklamak için DATE veri tipi kullanabilirsiniz.

-_TIME_: Sadece saat bilgisini saklar, "12:30:15" gibi. Bir siparişin saatini saklamak için TIME veri tipi kullanabilirsiniz.

-_DATETIME_: Tarih ve saat bilgisini birlikte saklar, "2022-12-31 12:30:15" gibi. Bir haberin yayınlanma tarihini saklamak için DATETIME veri tipi kullanabilirsiniz.

-_TIMESTAMP_: Tarih ve saat bilgisini birlikte saklar ve ayrıca bu bilgilerin hangi zaman diliminde olduğunu da saklar. Örneğin, "2022-12-31 12:30:15 UTC" gibi. 
Bir gönderinin zaman damgasını saklamak için TIMESTAMP veri tipi kullanabilirsiniz.

-_INTERVAL_: Zaman aralığını saklar. Örneğin "2 years 3 months 4 days" gibi. Bir projenin süresini saklamak için INTERVAL veri tipi kullanabilirsiniz.

**Array Veri Tipi**

SQL veritabanlarında, array veri tipleri bir dizi (koleksiyon) içinde birden çok veriyi saklamak için kullanılır. Array veri tipleri, bir kolon içinde birden çok 
veriyi saklamak için kullanılabilir ve genellikle bir tablo içinde bir kullanıcının birden çok özelliğini saklayabilir. Örneğin bir web sitesindeki kullanıcının 
bir veya birden çok telefon numarasını saklamak için array veri tipi kullanılabilir.


**2.Veri Tabanlarında Anahtar (Key) Kavramı**

İlişkisel veritabanları, verileri saklamak ve sorgulamak için SQL (Structured Query Language) kullanır. Veritabanlarında oluşturduğumuz tablonun bir diğer tablo ile ilişki kurabilmesi için anahtar kavramını anlamak gerekir. 

-_Primary Key (Birincil Anahtar)_

Primary Key (Birincil Anahtar) bir veri tabanında bir tablo içerisindeki her bir kaydı benzersiz bir şekilde tanımlamak için kullanılan bir anahtardır. Birincil anahtar, tablodaki diğer anahtarlar primary key'den referans alır. 

-_Foreign Key (Yabancı Anahtar)_

Foreign Key (Yabancı Anahtar) SQL'de bir başka tablonun birincil anahtarına bağlantı kurmak için kullanılan anahtardır. Foreign key, ilişkisel veri tabanlarında tablolar arasında ilişki tanımlamak için kullanılır.

Foreign key ile:
- Veri tabanındaki tablolar arasında ilişki kurulur.
- Veri güvenliği sağlanır.
- Veri kalitesi sağlanır.
- Veri normalizasyonu sağlanır.

![266414340-b30f0bd5-18cf-480a-b9d4-0d4f2cc6c7fc](https://github.com/SinanKosoglu/SinanKosoglu/assets/140150167/baa0feb4-c1a2-42f2-8618-d19d6aa4350f)

**3.SQL'de Temel Operatörler**

-_CREATE Komutu_

SQL'de, CREATE komutu veritabanı veya tablolarda yeni bir tablo oluşturmak için kullanılır. 

Tablo oluşturmak için genel kullanım şekli şöyledir:

    CREATE TABLE tablo_ismi (

       kolon1_ismi veri_tipi,

       . . .

    );

test_db isimli bir database oluşturmak ve bu database'de bir tablo tanımlamak için aşağıdaki işlemler yapılır;

    create database test_db; 

    create table ogrenci 
    ( 
      id integer, 
      isim varchar(30), 
      soyisim varchar(30), 
      primary key (id) 
    )
    ;
    create table ders
    ( 
       id integer primary key, 
       name varchar(30), 
       ogrenci_id integer 
       foreign key (pgrenci_id) references ogrenci(id) 
    )
    ;
    create table ogretmenler
    (
      isim varchar(30),
      soyisim varchar(30),
      ogretmen_id integer
    )
    
    -_ALTER/DROP Komutu_

- SQL'de, ALTER komutu veritabanı veya tablolarda mevcut olan tablonun yapısını veya özelliklerini değiştirmek için kullanılır. Genel olarak ALTER komutu ile tablolara kolon ekleme, kolon silme, kolon ismini değiştirme, kolon veri tipini değiştirme, constraint ekleme veya silme gibi işlemler yapılabilir. 

- SQL'de, DROP komutu veritabanı veya tablolarda mevcut olan tablo, index, view, procedure, trigger, sequence, synonym, domain, role, constraint gibi veritabanı objelerini silmek için kullanılır.

ALTER Kullanım Örnekleri:

    ALTER TABLE calisanlar ADD COLUMN cinsiyet VARCHAR(10) ---calisanlar tablosuna cinsiyet isimli kolon ekler.
    ALTER TABLE calisanlar DROP COLUMN cinsiyet ---calisanlar tablosundan cinsiyet isimli kolonu siler. 
    ALTER TABLE calisanlar RENAME COLUMN ad TO isim ---calisanlar tablosunda ad isimli sütunu isim olarak değiştirir.

ALTER komutu sadece tablolara değil aynı zamanda veritabanlarına da uygulanabilir. Örneğin;

    ALTER DATABASE veritabani_ismi SET default_character_set = utf8

- Genel olarak ALTER komutu ile tablolara kolon ekleme, kolon silme, kolon ismini değiştirme, kolon veri tipini değiştirme, constraint ekleme veya silme gibi işlemler yapılabilir.

- Constraint yani kısıtlamalar tabloya girebilecek veri türünü kısıtlamak için kullanılır.

  alter table ders add column ogretmen varchar(30)
;
  alter table ders alter ogretmen type varchar (50)
;
  alter table ders drop column ogretmen
;
  alter table ogretmen add constraint ogretmen_pkey primary key (ogretmen_id)
;
  alter table ogretmen drop constraint ogretmen_pkey primary key (ogretmen_id)
;
  alter table ogretmen rename to ogretmenler

```

- Aşağıdaki tablolarda, önce tabloları ekleyip arkasından kısıtlama eklenmiştir. Foreign key’i ‘ogrenci’ tablosunda ‘course_id’ yaparak diğer tabloda bağlanılan sütun referans gösterilmiştir.

create table ogrenci
(
ogrenci_id integer not null primary key,
isim varchar(30),
soyisim varchar(30),
course_id integer
)

create table course_info
(
course_id integer not null primary key,
course_title varchar(150)
)

alter table ogrenci add constraint course_id_fkey foreign key (course_id) references course_info (course_id)
alter table ogrenci drop constraint course_id_fkey
```

DROP Kullanım Örnekleri:

    DROP TABLE table_name;
    DROP INDEX index_name;
    DROP VİEW view_name;
    DROP PROCEDURE procedure_name;
    DROP TRIGGER trigger_name;
    DROP SEQUENCE sequence_name;
    DROP SYNONYM synonym_name;
    DROP DOMAIN domain_name;
    DROP ROLE role_name;
    DROP CONSTRAINT constraint_name;
 
- DROP; belirtilen tablo, index, view, procedure, trigger, sequence, synonym, domain, role, constraint gibi veritabanı objelerini veritabanından tamamen siler.

-_INSERT/COPY Komutu_

- SQL'de, INSERT komutu veritabanı veya tablolarda mevcut olan tablo'ya yeni veri eklemek için kullanılır.

      INSERT INTO table name values 
      ( 
        'ad', 
        'soyad', 
        yas 
      )
  
      INSERT INTO ogrenci VALUES 
        (21,'sinan','kosoglu'),
        (22,'kara','mehmet'),
        (23,'sara','sara'),
        (24,'mehmet','kosoglu'),
        (25,'Sabine','Korur')

  - COPY komutu, veritabanındaki bir tablonun verilerini veya verileri içeren bir dosyadan veritabanına veri yüklemek için kullanılır. Bu komut genellikle çok hızlı ve büyük veri setlerinin yüklenmesi için kullanılır.

      COPY quiz_info FROM 'C:\Program Files\PostgreSQL\15\bin\365_quiz_info.csv' delimiter ',' csv header
  - Bu komut ile belirtilen uzantı yolundan ',' virgül delimiter ile csv uzantılı bir dosyadan quiz_info dosya isminin veritabanına yüklenileceğini gösteriyor.

-_UPDATE Komutu_

- SQL'de, UPDATE komutu veritabanı veya tablolarda mevcut olan tabloda bulunan verileri güncellemek için kullanılır.

      UPDATE ogrenci
      SET soyisim = 'kosoglu'
      WHERE id = 23
      ;
      UPDATE ogrenci
      SET vize1 = 75, vize2 = 88, final = 100 
      WHERE id = 23

!!Update komutlarında where operatörünün yeri çok önemlidir. Eğer where komutu kullanılmaz ise belirli bir alan değil soyisimi bütün verilerin 'Kosoglu' yapacaktır. 2. örnekte ise eğer id=23 belirtilmeseydi bütün sütunların notlarını gösterilen gibi değiştirecektir. 

-_TRUNCATE/DELETE Komutu_

- SQL'de, TRUNCATE komutu veritabanı veya tablolarda mevcut olan tablonun verilerini silmek için kullanılır. Bu komut, veritabanındaki bir tablonun tüm satırlarını veya kayıtlarını hızlı bir şekilde siler.

      TRUNCATE ogrenci
      ;
      TRUNCATE quiz_info

- SQL'de, DELETE komutu veritabanı veya tablolarda mevcut olan tablonun verilerini silmek için kullanılır. Bu komut, veritabanındaki bir tablonun belirli satırlarını veya kayıtlarını siler.

      DELETE FROM ogrenci WHERE id = 25

- Yukarıdaki sorgu aynı UPDATE sorgusunda olduğu gibi WHERE koşulu ile filtreleme yapar. Eğer WHERE id = 25 filtresi kullanılmasaydı tablodaki tüm veriler silinirdi. Bu nedenle UPDATE komutunda olduğu gibi DELETE komutunda da WHERE koşulu da çok önemlidir. 

-_SELECT Komutu & Aritmetik Fonksiyonlar_

- SQL'de, SELECT komutu veritabanı veya tablolarda mevcut olan verileri sorgulamak için kullanılır. Bu komut, veritabanındaki bir tablonun veya birden fazla tablonun belirli satırlarını veya kayıtlarını seçerek döndürür.
  
      SELECT *
      FROM ogrenci
      ;
      SELECT isim, soyisim
      FROM ogrenci

![aritmetik işlemler tablosu](https://github.com/SinanKosoglu/SinanKosoglu/assets/140150167/48c95b79-3db6-46f6-be1d-32c9b313857d)

Ondalıklı işlemlerde ;

    SELECT 4.3534534-3.242352
    SELECT 45.0/4.0

- Float olarak almak için ondalıklı olarak yazılması gerekiyor. (.) nokta kullanılıyor. virgül değil!!
  
      UPDATE ogrenci
      SET vize1 = 75, vize2 = 88, final = 100 
      WHERE id = 23

**4.String Functions & Case When & Other Clauses**

_STRING FUNCTIONS (Metinsel Fonksiyonlar)_

- SQL'de string fonksiyonlar, karakter dizisi (string) verileri üzerinde işlemler yapmak için kullanılan işlevlerdir. Bu fonksiyonlar, string verilerini manipüle etmek, dönüştürmek veya karşılaştırmak için kullanılabilirler.
- Bu fonksiyonlar, SQL sorgularında kullanılan WHERE, SELECT, ORDER BY ve GROUP BY gibi ifadelerde sıklıkla kullanılırlar. Örneğin, bir tablodaki bir sütunun değerini kesmek veya birleştirmek, bir karakter dizisinde belirli bir alt dizenin konumunu bulmak veya belirli bir harf veya harf dizisini içeren tüm değerleri seçmek gibi işlemler için kullanılabilirler.
- Metinsel fonksiyonlar, verilerin manipülasyonunu daha kolay hale getirerek verilerin analiz edilmesini ve raporlanmasını kolaylaştırır. Ayrıca, birçok programlama dili ve veritabanı yönetim sistemi, metinsel fonksiyonlar da dahil olmak üzere string işleme için çeşitli fonksiyonlar sağlamaktadır.

*-CONCAT*

- PostgreSQL'de CONCAT()  fonksiyonu, verilen iki veya daha fazla dizeyi BİRLEŞTİREREK tek bir dize oluşturur. Fonksiyonun kullanımı şu şekildedir:

      SELECT concat(first_name, ' ', last_name) as full_name FROM employees;

- Concat fonksiyonu, özellikle metinleri birleştirmek gerektiği durumlarda kullanışlıdır. Ayrıca, concat fonksiyonu yerine || operatörü de kullanılabilir. Bu operatör de aynı şekilde iki dizeyi birleştirir:

string1 || string2

*-LEFT*

- LEFT()  fonksiyonu, verilen bir dizenin belirli bir sayıda sol karakterini EKRANA GETİRİR. Fonksiyonun kullanımı şu şekildedir:

      SELECT left(first_name, 3) as initial FROM employees; ---first_name sütunundan veri alır ve ilk üç karakterini EKRANA GETİRİR.

*-RIGHT*

- RIGHT fonksiyonu, verilen bir dizenin belirli bir sayıda sağ karakterini EKRANA GETİRİR. Fonksiyonun kullanımı şu şekildedir:

      SELECT right(phone_number, 4) as last_four_digits FROM employees; --phone sütunundan veri alır ve son dört karakterini EKRANA GETİRİR.

*-LENGTH*

- LENGTH() fonksiyonu, bir karakter dizisinin uzunluğunu döndüren bir fonksiyondur. Yani, bu fonksiyon bir karakter dizisindeki karakterlerin sayısını sayar.

      SELECT length(first_name), first_name FROM employees; --first_name'in karakter uzunluğunu verir.

*-LOWER*

- PostgreSQL'de LOWER() fonksiyonu, bir karakter dizisindeki tüm karakterleri küçük harflere dönüştürür.

      SELECT LOWER(first_name), LOWER(last_name) FROM employees;

*-UPPER*

- PostgreSQL'de UPPER() fonksiyonu, bir karakter dizisindeki tüm karakterleri büyük harflere dönüştürür.

      SELECT UPPER(first_name) AS first_name_upper, UPPER(last_name) AS last_name_upper FROM employees ORDER BY last_name_upper, first_name_upper;

*-TRIM*

- PostgreSQL'de TRIM() fonksiyonu, bir karakter dizisindeki boşlukları, belirtilen karakterleri veya karakter dizisini kırparak temizler."LEADING", "TRAILING" ve "BOTH" parametreleri, bu karakterleri nereden kaldıracağını belirtir.

TRIM([LEADING | TRAILING | BOTH] trim_character FROM string)

Örnekler:

    SELECT TRIM('   hello   '); -- "hello" 
    SELECT TRIM(LEADING '0' FROM '0001234'); -- "1234" 
    SELECT TRIM(TRAILING '!' FROM 'hello!!!!'); -- "hello" 
    SELECT TRIM(BOTH ' ' FROM '   hello   '); -- "hello"

Trim (Leading from string) —> Baştan 

Trim (Trailing from string) —> Sondan

Trim (Both from string) —> Her iki taraftan

	SELECT TRIM (LEADING
	FROM '  PostgreSQL TRIM'),
	TRIM (TRAILING
	FROM 'PostgreSQL TRIM   '),
	TRIM ('  PostgreSQL TRIM  ');

  ![Untitled](https://github.com/SinanKosoglu/SinanKosoglu/assets/140150167/2076a4a8-4af3-42c3-9297-6b7155037d27)

UPDATE customer
SET
  first_name = TRIM(first_name),
  last_name = TRIM(last_name);

Update edilmesi gereken bir durum olarak isim ve soyisimlerin önünde ve arkasında bulunan boşlukları kırpar ve günceller. 

*-REPLACE*

- PostgreSQL'deki REPLACE() fonksiyonu, bir karakter dizisinde belirli bir karakter dizisini bulur ve onu başka bir karakter dizisiyle değiştirir.
- Eksik yani tamamlanmamış bir veriyi değiştirmeye yarıyor. Örneğin; ‘stanbul’ yazısını ‘istanbul’ yapmak gibi.

      SELECT REPLACE(alan_adi, degisecek_veri, yeni_veri) FROM tablo_adı

      SELECT REPLACE(first_name, 'a', 'o'), REPLACE(last_name, 'a', 'o') FROM employees; --Tüm çalışanların isimlerindeki "a" harfini "o" harfi ile değiştirir. 

      SELECT REPLACE(email, 'sqltutorial.org', 'yahoo.com') FROM employees; -- e-posta adreslerindeki "sqltutorial.org" uzantısını "yahoo.com" ile  değiştirir.

*-SPLIT PART*

- PostgreSQL'deki SPLIT_PART() fonksiyonu, bir karakter dizisini belirli bir ayraç karakterine göre parçalar ve parçalardan birini seçer.
- “delimiter" bir ayraç karakteridir. 
  
      SELECT SPLIT_PART (string, delimiter, field) FROM tablo_adı

      SELECT SPLIT_PART(email, '@', 1) AS username FROM employees
  
SELECT SPLIT_PART(email, '@', 1) AS username FROM employees; --employees tablosundaki email adreslerini @ işaretini baz alarak iki parçaya ayırır ve 1. parçayı seçer. Böylece mail adreslerindeki ilk kısım kullanıcı adı olarak belirlenir. 

_CASE WHEN EXPRESSION_

- "CASE WHEN" SQL'de koşul ifadesi ile kullanılan bir kontrol yapısıdır.  Bu ifade, belirli bir koşulu test etmenizi ve koşulun doğru veya yanlış olmasına bağlı olarak farklı bir değer veya ifade döndürmenizi sağlar.

      CASE 

      WHEN condition1 THEN result1 

      WHEN condition2 THEN result2 

      ... 

      ELSE result 

      END

Örnek olarak, employee tablosunda ki çalışanların isim, soyisim, kimlik id si ve salary leri getirilmesi isteniyor. Fakat, bunun yanında asgari maaş olanlar için yanına düşük maaş 20.000 altın ve asgari ye kadar olan kısm için ortalama maaş geriye kalan maaşlara da normal maaş yazısı yanlarına getirilmesi koşulları yazılmış. 

    SELECT
      EMPLOYEE_ID,
      FIRST_NAME,
      LAST_NAME,
      SALARY,
    CASE
      WHEN SALARY < 11402 THEN 'Dusuk Maas'
      WHEN SALARY >= 11402
        AND SALARY < 20000 THEN 'Ortalama Maas'
          ELSE 'Normal'
         END
    FROM EMPLOYEES;

Örnek olarak, Bu sefer yanlarına maaşlara zamlı halleri ile getirilmesi için komutlar koşullar yazılmış. Maaş zamlarını belirlemek için asgari maaş, 20.000 tl ye kadar olan maaşlar ve geriye kalan maaşların zam oranları ve zamlı hallerini gösteriyor. 
      SELECT
        EMPLOYEE_ID,
        FIRST_NAME,
        LAST_NAME,
        SALARY,
      CASE
        WHEN SALARY < 11402 THEN SALARY * 1.5
        WHEN SALARY >= 11402
           AND SALARY < 20000 THEN SALARY * 1.25
            ELSE SALARY * 1.15
          END
      FROM EMPLOYEES;

Örnek olarak, bir "customers" tablosunda "city" sütunu bulunuyor ve müşterilerin yaşadıkları şehirleri sorgulamak istiyoruz. Aynı zamanda, bazı müşterilerin yaşadıkları şehirlerin yanlış yazıldığı fark ediliyor. Bu durumda, aşağıdaki örnek SQL sorgusu ile müşterilerin doğru şehirlerini elde edebiliriz:

    SELECT 

    customer_name, 

    CASE 

        WHEN city = 'Istanbl' THEN 'Istanbul' 

        WHEN city = 'Ankra' THEN 'Ankara'

        ELSE city 

    END AS city_corrected  

    FROM customers;

Örneğin, bir müşteri veritabanında, bir müşterinin ülkesine göre farklı vergi oranları uygulanması gerekiyorsa, "CASE WHEN" ifadesi kullanılabilir. Aşağıdaki örnek, bir müşterinin ülkesine göre farklı vergi oranları uygulayan bir sorgudur:

    SELECT name, country, 

       CASE WHEN country = 'USA' THEN price * 0.08 

            WHEN country = 'Canada' THEN price * 0.10 

            ELSE price * 0.12 

       END AS tax 

    FROM customers;

_OTHER CLAUSES (ORDER BY, AS, LIMIT, DISTINCT, HAVING)_

*-ORDER BY*

- SQL'de ORDER BY komutu, veritabanındaki belirli bir tablo veya sütun içindeki kayıtların belirli bir kriterlere göre sıralanmasını sağlar. Örneğin, müşterilerin adlarına göre sıralamak istediğinizde veya satışların tarih sırasına göre sıralamak istediğinizde ORDER BY kullanabilirsiniz.

      SELECT * FROM orders ORDER BY order_date,total_price; --"orders" tablosundaki siparişlerin tarih ve tutar sırasına göre sıralanmış halde döndürür.
     ; 
      SELECT * FROM employees ORDER BY hire_date -- "employees" tablosunda ki çalışanların işe alım zamanlarına göre ilk sıradan başlayarak sıralanmış halde ekrana getirecektir.
  
ASC: küçükten büyüğe
DESC: büyükten küçüğe

*-AS*

- SQL'de AS komutu, sorgularda kullanılan sütun veya tablo adlarının yerine farklı bir isim vermenizi sağlar. Bu, sorguların daha okunaklı ve anlaşılır olmasını sağlar. Örneğin, bir tablonun adı uzun ve anlaşılmazsa, bu tablonun sorgularda kullanılması için kısa ve anlaşılır bir ad vermeniz mümkündür.

      SELECT SUM(total_price) AS 'Total Sales' FROM orders; -- "orders" tablosundaki siparişlerin toplam tutarını döndürür ve sütun adını "Total Sales" olarak değiştirir. Aynı zamanda AS komutu ile tablo adlarınıda değiştirebilirsiniz. <br></br>

      SELECT * FROM customers AS 'Müşteriler' --"customers" tablosunun adını "Müşteriler" olarak değiştirir.

    SELECT employee_id,
      first_name,
      last_name,
      salary,
    CASE
       WHEN salary < 8500                     THEN salary1.5
       WHEN salary >= 8500 AND salary < 15000 THEN salary1.25
    ELSE salary*1.15
      END AS new_salary -- case when sütununun aliası olarak atanır.
      FROM employees AS e -- tablonun aliasını değiştirir. tablo join komutlarında kullanılabilir. 

*-LIMIT*

- LIMIT, SQL sorgularında sorgunun sonucunda döndürülecek olan satır sayısını belirlemek için kullanılan bir ifadedir. Örneğin, veritabanındaki tüm müşteri kayıtlarını almak yerine sadece ilk 10 kaydı almak isteyebilirsiniz. Bu durumda, sorgunun sonunda LIMIT 10 kullanılır.

      SELECT * FROM customers LIMIT 10;

- Ayrıca, LIMIT ile OFFSET kullanarak belirli bir aralıkta kayıtları alabilirsiniz. Örneğin, 21. ila 30. müşteri kayıtlarını almak için:

      SELECT * FROM customers LIMIT 10 OFFSET 20; -customers tablosundaki 21. ila 30. kayıtları döndürür.

*-DISTINCT*

- DISTINCT, SQL sorgularında veritabanındaki aynı değerleri tekrar etmeden sadece farklı değerleri döndürmek için kullanılan bir ifadedir. Örneğin, veritabanındaki tüm müşteri kayıtlarını almak yerine sadece farklı müşteri adlarını almak isteyebilirsiniz. Bu durumda, sorgunun başına DISTINCT yazılır.

      SELECT DISTINCT name FROM customers;
      SELECT city, COUNT(DISTINCT name) FROM customers GROUP BY city; --customers tablosundaki tüm farklı şehirleri ve bu şehirlerde yaşayan farklı müşteri sayılarını döndürür.
  
      SELECT DISTINCT
        job_id,
        department_id
      FROM employees
      ORDER BY job_id DESC;
  
*-HAVING*

-  WHERE anahtar sözcüğü aggregate fonnksiyonlarıyla kullanılamadığı için HAVING SQL diline eklenmiştir. Kullanımı aşağıdaki gibidir:

        SELECT column_name(s)
        FROM table_name
        WHERE condition
        GROUP BY column_name(s)
        HAVING condition
        ORDER BY column_name(s);

       SELECT COUNT(CUstumerID), Country
       FROM Customers
       GROUP BY Country
       HAVING COUNT(CustomerID)>5;

- Yukarıdaki sorguda her ülkeddeki müşteri sayısı listelenir ve müşteri sayısı 5'ten fazla olan ülkeler seçilir. 
     
      SELECT COUNT(CustomerID), Country
      FROM Customers
      GROUP BY Country
      HAVING COUNT(CustomerID) > 5
      ORDER BY COUNT(CustomerID) DESC;

- Yukarıdaki sorguda müşteri sayısı 5'ten fazla olan ülkeler azalan şekilde sıralanır. COUNT(CostumerID) Where koşuluyla birlikte kullanılmaz. Bunun yerine GROUP BY HAVING ifadesi kullanılır.
- HAVING, group by komutundan sonra kullanılır. WHERE, group by komutundan önce kullanılır.

**-WHERE Komutu ve Karşılaştırma Operatörleri**

- WHERE komutu sorgulama işlemi sırasında belirli koşullara göre verileri filtrelemeye yarar.


SELECT * FROM tablo_adi WHERE sartlar


**-Eşittir Operatörü (=)**

SQL'de WHERE komutu içinde kullanılan "=" (eşittir) operatörü, belirli bir kriterde eşit olan verileri seçmek için kullanılır. Örneğin, "employees" tablosundaki "last_name" sütununda "Smith" değerini içeren kayıtları seçmek için aşağıdaki sorguyu kullanabilirsiniz:

SELECT * FROM employees WHERE age = 25;

SELECT * FROM employees WHERE first_name = 'Nancy'
SELECT * FROM employees WHERE employee_id = 105

**Eşit Değildir Operatörü (<> ya da !=)**

SQL'de WHERE komutu içinde kullanılan "<>" (eşit değildir) operatörü, belirli bir kriterde eşit olmayan verileri seçmek için kullanılır. Örneğin, "employees" tablosundaki "last_name" sütununda "Smith" değerini içermeyen kayıtları seçmek için aşağıdaki sorguyu kullanabilirsiniz:

SELECT * FROM employees WHERE employee_id != 105

Bu sorgu "employees" tablosundaki tüm kayıtları seçer ve sadece "last_name" sütununda "Smith" değerini içermeyen kayıtları gösterir.

Aynı şekilde "age" sütununda 25 değerini içermeyen kayıtları seçmek için:

SELECT * FROM employees WHERE age <> 25;

SELECT * FROM employees WHERE last_name <> 'Smith';
SELECT * FROM employees WHERE employee_id <> 105

Bu sorgu "employees" tablosundaki tüm kayıtları seçer ve sadece "age" sütununda 25 değerini içermeyen kayıtları gösterir.

**Büyüktür Operatörü (>)**

SQL'de WHERE komutu içinde kullanılan ">" (büyüktür) operatörü, belirli bir kriterde büyük olan verileri seçmek için kullanılır. Örneğin, "employees" tablosundaki "age" sütununda 25 değerinden büyük olan kayıtları seçmek için aşağıdaki sorguyu kullanabilirsiniz:

```sql
SELECT * FROM employees WHERE age > 25;
```

Bu sorgu "employees" tablosundaki tüm kayıtları seçer ve sadece "age" sütununda 25 değerinden büyük olan kayıtları gösterir.

```sql
SELECT first_name, last_name FROM employees WHERE job_id > 6 
```

Aynı şekilde "salary" sütununda 50000 değerinden büyük olan kayıtları seçmek için:

```sql
SELECT * FROM employees WHERE salary > 50000;
```

Bu sorgu "employees" tablosundaki tüm kayıtları seçer ve sadece "salary" sütununda 50000 değerinden büyük olan kayıtları gösterir.

## Büyük ya da Eşittir Operatörü (>=)

```sql
SELECT * FROM employees WHERE hire_date >= '1997-01-01'
```

## **Küçüktür Operatörü (<)**

SQL'de WHERE komutu içinde kullanılan "<" (küçüktür) operatörü, belirli bir kriterde küçük olan verileri seçmek için kullanılır. Örneğin, "employees" tablosundaki "age" sütununda 25 değerinden küçük olan kayıtları seçmek için aşağıdaki sorguyu kullanabilirsiniz:

```sql
SELECT * FROM employees WHERE age < 25;
```

Bu sorgu "employees" tablosundaki tüm kayıtları seçer ve sadece "age" sütununda 25 değerinden küçük olan kayıtları gösterir.

Aynı şekilde "salary" sütununda 50000 değerinden küçük olan kayıtları seçmek için:

```sql
SELECT * FROM employees WHERE salary < 50000;
```

Bu sorgu "employees" tablosundaki tüm kayıtları seçer ve sadece "salary" sütununda 50000 değerinden küçük olan kayıtları gösterir.

## **Küçük ya da Eşittir Operatörü (<=)**

SQL'de WHERE komutu içinde kullanılan "<=" (küçük ya da eşittir) operatörü, belirli bir kriterde küçük veya eşit olan verileri seçmek için kullanılır. Örneğin, "employees" tablosundaki "age" sütununda 25 değerinden küçük ya da eşit olan kayıtları seçmek için aşağıdaki sorguyu kullanabilirsiniz:

```sql
SELECT * FROM employees WHERE age <= 25;
```

Bu sorgu "employees" tablosundaki tüm kayıtları seçer ve sadece "age" sütununda 25 değerinden küçük ya da eşit olan kayıtları gösterir.

Aynı şekilde "salary" sütununda 50000 değerinden küçük ya da eşit olan kayıtları seçmek için:

```sql
SELECT * FROM employees WHERE salary <= 50000;
```

Bu sorgu "employees" tablosundaki tüm kayıtları seçer ve sadece "salary" sütununda 50000 değerinden küçük olan kayıtları gösterir.

## **IS NULL Operatörü (IS NULL)**

SQL'de WHERE komutu içinde kullanılan "IS NULL" operatörü, belirli bir sütunda NULL değerinin olup olmadığını kontrol etmek için kullanılır. Örneğin, "employees" tablosundaki "phone" sütununda NULL değerinin olup olmadığını kontrol etmek için aşağıdaki sorguyu kullanabilirsiniz:

```sql
SELECT * FROM employees WHERE phone IS NULL;
```

Bu sorgu "employees" tablosundaki tüm kayıtları seçer ve sadece "phone" sütununda NULL değeri olan kayıtları gösterir.

Aynı şekilde "email" sütununda NULL değerinin olup olmadığını kontrol etmek için:

```sql
SELECT * FROM employees WHERE email IS NULL;
```

Bu sorgu "employees" tablosundaki tüm kayıtları seçer ve sadece "email" sütununda NULL değeri olan kayıtları gösterir.

## **AND (VE) Operatörü**

SQL'de WHERE komutu içinde kullanılan "AND" operatörü, birden fazla kriterin aynı anda gerçekleşmesini sağlamak için kullanılır. Örneğin, "employees" tablosundaki "age" sütununda 25 değerinden küçük ve "salary" sütununda 50000 değerinden büyük olan kayıtları seçmek için aşağıdaki sorguyu kullanabilirsiniz:

```sql
SELECT * FROM employees WHERE age < 25 AND salary > 50000;
```

Bu sorgu "employees" tablosundaki tüm kayıtları seçer ve sadece "age" sütununda 25 değerinden küçük ve "salary" sütununda 50000 değerinden büyük olan kayıtları gösterir.

Aynı şekilde "employees" tablosundaki "gender" sütununda 'Female' ve "phone" sütununda NULL değerinin olup olmadığını kontrol etmek için:

```sql
SELECT * FROM employees WHERE gender = 'Female' AND phone IS NULL;
```

Bu sorgu "employees" tablosundaki tüm kayıtları seçer ve sadece "gender" sütununda 'Female' ve "phone" sütununda NULL değeri olan kayıtları gösterir.

## **OR (VEYA) Operatörü**

SQL'de WHERE komutu içinde kullanılan "OR" operatörü, birden fazla kriterin en az birinin gerçekleşmesini sağlamak için kullanılır. Örneğin, "employees" tablosundaki "age" sütununda 25 değerinden küçük veya "salary" sütununda 50000 değerinden büyük olan kayıtları seçmek için aşağıdaki sorguyu kullanabilirsiniz:

```sql
SELECT * FROM employees WHERE age < 25 OR salary > 50000;
```

Bu sorgu "employees" tablosundaki tüm kayıtları seçer ve sadece "age" sütununda 25 değerinden küçük veya "salary" sütununda 50000 değerinden büyük olan kayıtları gösterir.

Aynı şekilde "employees" tablosundaki "gender" sütununda 'Female' veya "phone" sütununda NULL değerinin olup olmadığını kontrol etmek için:

```sql
SELECT * FROM employees WHERE gender = 'Female' OR phone IS NULL;
```

Bu sorgu "employees" tablosundaki tüm kayıtları seçer ve sadece "gender" sütununda 'Female' veya "phone" sütununda NULL olan kayıtları gösterir.

## **IN (İÇİNDE) Operatörü**

SQL'de WHERE komutu içinde kullanılan "IN" operatörü, belirli değerler için arama yapmak için kullanılır. Örneğin, "employees" tablosundaki "age" sütununda 25, 30 ve 35 değerlerinden birinin olup olmadığını kontrol etmek için aşağıdaki sorguyu kullanabilirsiniz:

```sql
SELECT * FROM employees WHERE age IN (25, 30, 35);
```

Bu sorgu "employees" tablosundaki tüm kayıtları seçer ve sadece "age" sütununda 25, 30 veya 35 değerlerinden birinin olan kayıtları gösterir.

Aynı şekilde "employees" tablosundaki "gender" sütununda 'Female' veya "Male" değerlerinin olup olmadığını kontrol etmek için:

```sql
SELECT * FROM employees WHERE gender IN ('Female', 'Male');
```

Bu sorgu "employees" tablosundaki tüm kayıtları seçer ve sadece "gender" sütununda 'Female' veya 'Male' değerlerinden birinin olan kayıtları gösterir.

## **BETWEEN (ARASINDA) Operatörü**

SQL'de WHERE komutu içinde kullanılan "BETWEEN" operatörü, belirli bir değer aralığı içinde arama yapmak için kullanılır. Örneğin, "employees" tablosundaki "age" sütununda 25 ve 35 arasındaki değerlerin olup olmadığını kontrol etmek için aşağıdaki sorguyu kullanabilirsiniz:

```sql
SELECT * FROM employees WHERE age BETWEEN 25 AND 35;
```

Bu sorgu "employees" tablosundaki tüm kayıtları seçer ve sadece "age" sütununda 25 ve 35 arasındaki değerlerden birinin olan kayıtları gösterir.

Aynı şekilde "employees" tablosundaki "salary" sütununda 40000 ile 60000 arasındaki değerlerin olup olmadığını kontrol etmek için:

```sql
SELECT * FROM employees WHERE salary BETWEEN 40000 AND 60000;
```

Bu sorgu "employees" tablosundaki tüm kayıtları seçer ve sadece "salary" sütununda 40000 ile 60000 arasındaki değerlerden birinin olan kayıtları gösterir.

## **LIKE (BENZER) Operatörü**

SQL'de WHERE komutu içinde kullanılan "LIKE" operatörü, belirli bir kalıp içinde arama yapmak için kullanılır. Örneğin, "employees" tablosundaki "name" sütununda "J%" harfleri ile başlayan isimlerin olup olmadığını kontrol etmek için aşağıdaki sorguyu kullanabilirsiniz.

```sql
SELECT * FROM employees WHERE name LIKE 'J%';
```

Bu sorgu "employees" tablosundaki tüm kayıtları seçer ve sadece "name" sütununda "J%" harfleri ile başlayan isimlerin olan kayıtları gösterir.

Aynı şekilde "employees" tablosundaki "email" sütununda "@gmail.com" ile biten değerlerin olup olmadığını kontrol etmek için:

```sql
SELECT * FROM employees WHERE email LIKE '%@gmail.com';
```

Bu sorgu "employees" tablosundaki tüm kayıtları seçer ve sadece "email" sütununda "@gmail.com" ile biten değerlerin olan kayıtları gösterir.

"_" kullanarak herhangi bir karakteri temsil edebilirsiniz. Örnek olarak "employees" tablosundaki "name" sütununda "J_n" harfleri ile başlayan isimlerin olup olmadığını kontrol etmek için:

```sql
SELECT * FROM employees WHERE name LIKE 'J_n';
```

Bu sorgu "employees" tablosundaki tüm kayıtları seçer ve sadece "name" sütununda "J_n" harfleri ile başlayan isimlerin olan kayıtları gösterir.

## **NOT (DEĞİL) Operatörü**

SQL'de NOT operatörü, bir koşulun tersini ifade eder.

Örneğin "employees" tablosundaki "age" sütununda 18 veya 60'dan küçük olan değerlerin olup olmadığını kontrol etmek için:

```sql
SELECT * FROM employees WHERE NOT (age < 18 OR age > 60);
```

Bu sorgu "employees" tablosundaki tüm kayıtları seçer ve sadece "age" sütununda 18 veya 60'dan küçük değerlerin olmayan kayıtları gösterir.

NOT operatörü genellikle NOT NULL, NOT IN, NOT BETWEEN gibi koşullar için kullanılabilir.

Örnek olarak "employees" tablosundaki "phone" sütununda NULL değerlerinin olmadığını kontrol etmek için:

```sql
SELECT * FROM employees WHERE NOT phone IS NULL;
```

Bu sorgu "employees" tablosundaki tüm kayıtları seçer ve sadece "phone" sütununda NULL  olmayan kayıtları gösterir.

*-WHERE Komutu ve LIKE Operatörü*

- J ile başlayan isimler:

      SELECT * FROM employees WHERE name LIKE 'J%';

- @gmail.com ile biten mail adresleri:

      SELECT * FROM employees WHERE email LIKE '%@gmail.com';

- Aşağıdaki sorgu "employees" tablosundaki tüm kayıtları seçer ve sadece "name" sütununda "J_n" harfleri ile başlayan isimlerin olan kayıtları gösterir.

      SELECT * FROM employees WHERE name LIKE 'J_n';

- Aşağıdaki sorgu L ile başlayan, ardından bir joker karakter ardından nd ve ardından iki joker karakterle başlayan müşterileri döndürür:

      SELECT * FROM Customers
      WHERE city LIKE 'L_nd__';

  **5.Aggregate Functions (Toplu Fonksiyonlar)**

- SQL'de Aggregate Functions (Toplu Fonksiyonlar), bir tablonun birden fazla satırındaki verileri tek bir değer olarak özetler. Bunlar genellikle COUNT, SUM, AVG, MAX, MIN gibi fonksiyonlardır. Bu fonksiyonlar sadece SELECT sorgularında kullanılabilir ve genellikle GROUP BY komutu ile birlikte kullanılır.

*-COUNT()*

- "employees" tablosunda kaç tane kayıt olduğunu hesaplamak için aşağıdaki sorguyu kullanabiliriz:

      SELECT COUNT(*) FROM employees;
  
- manager_id'si 100 olan kaç çalışan olduğu aşağıdaki sorguyla listelenir:
  
      SELECT COUNT(employee_id) FROM employees WHERE manager_id= 100;

***COUNT fonksiyonu, NULL değerlerini saymaz. Eğer NULL değerleri dahil edilmek isteniyorsa COUNT(column_name) yerine COUNT(*) kullanılmalıdır.

*-COUNT() with GROUP BY*

- Aşağıdaki SQL sorgusu "employees" tablosundaki kişilerin departmanlara göre gruplandırılmış sayısını döndürür.

      SELECT department_id, COUNT(*) FROM employees GROUP BY department_id;

*-SUM, AVG & GROUP BY*

- SQL'de SUM fonksiyonu, bir tablonun belirli bir sütununda bulunan sayısal değerlerin toplamını hesaplar. Bu fonksiyon genellikle veritabanındaki verilerin toplamını belirlemek için kullanılır. SUM fonksiyonu sadece SELECT sorgularında kullanılabilir ve genellikle GROUP BY komutu ile birlikte kullanılır.

       SELECT department_id, SUM(salary) FROM employees GROUP BY department_id;

- SQL'de AVG fonksiyonu, bir tablonun belirli bir sütununda bulunan sayısal değerlerin ortalamasını hesaplar. Bu fonksiyon genellikle veritabanındaki verilerin ortalamasını belirlemek için kullanılır. AVG fonksiyonu sadece SELECT sorgularında kullanılabilir ve genellikle GROUP BY komutu ile birlikte kullanılır.

      SELECT department_id, AVG(salary) FROM employees GROUP BY department_id;

*-MIN, MAX & GROUP BY*

- SQL'de MAX fonksiyonu, bir tablonun belirli bir sütununda bulunan en yüksek değeri döndürür. Bu fonksiyon genellikle veritabanındaki verilerin en yüksek değerini belirlemek için kullanılır. MAX fonksiyonu sadece SELECT sorgularında kullanılabilir ve genellikle GROUP BY komutu ile birlikte kullanılır.

      SELECT MAX(salary) FROM employees WHERE department_id = 8;
      SELECT department_id, MAX(salary) FROM employees GROUP BY department_id;

- SQL'de MIN fonksiyonu, bir tablonun belirli bir sütununda bulunan en düşük değeri döndürür. Bu fonksiyon genellikle veritabanındaki verilerin en düşük değerini belirlemek için kullanılır. MIN fonksiyonu sadece SELECT sorgularında kullanılabilir ve genellikle GROUP BY komutu ile birlikte kullanılır.

      SELECT MIN(salary) FROM employees WHERE department_id = 3;
      SELECT department_id, MIN(salary) FROM employees GROUP BY department_id;


**6.SQL'de JOIN Komutu**

- SQL join işlemleri, bir veya daha fazla tablo arasında veri eşleme işlemidir. Tablolar arasındaki ilişkilere göre farklı join türleri bulunmaktadır.

  1. Inner Join: Veritabanındaki iki veya daha fazla tablo arasındaki eşleşen verilerin birleştirilmesini sağlar. Inner join, yalnızca ilişkili olan verilerin seçilmesine olanak tanır. İlişkili veriler, belirli bir kriter (örneğin, birleştirme anahtarı) üzerinden eşleştirilir. Eşleşmeyen veriler atılır ve sadece eşleşen veriler görüntülenir. Inner join, verileri birleştirirken verilerin verimli bir şekilde sorgulanmasını ve analiz edilmesini sağlar.
  2. Left Join: Veritabanındaki iki veya daha fazla tablo arasındaki verilerin birleştirilmesini sağlar. Left join, sol tablo içindeki tüm verileri ve sağ tablo ile eşleşen verileri seçer. Eşleşmeyen sağ tablo verileri NULL olarak görüntülenir. Bu tür bir join, sol tablo verilerinin tümünün görüntülenmesini ve eşleşmeyen sağ tablo verilerinin belirlenmesini sağlar. Left join, verilerin tamamının analiz edilmesi, raporlama veya veri keşfetme gibi amaçlar için kullanılabilir.
  3. Right Join: Veritabanındaki iki veya daha fazla tablo arasındaki verilerin birleştirilmesini sağlar. Right join, sağ tablo içindeki tüm verileri ve sol tablo ile eşleşen verileri seçer. Eşleşmeyen sol tablo verileri NULL olarak görüntülenir. Bu tür bir join, sağ tablo verilerinin tümünün görüntülenmesini ve eşleşmeyen sol tablo verilerinin belirlenmesini sağlar. Right join, verilerin tamamının analiz edilmesi, raporlama veya veri keşfetme gibi amaçlar için kullanılabilir.
  4. Full Outer Join: Veritabanındaki iki veya daha fazla tablo arasındaki verilerin tam birleştirilmesini sağlar. Full outer join, sol ve sağ tablodaki tüm verileri, her iki tablo arasındaki eşleşen ve eşleşmeyen verileri de dahil olmak üzere seçer. Eşleşmeyen veriler NULL olarak görüntülenir. Full outer join, verilerin tamamının analiz edilmesi, raporlama veya veri keşfetme gibi amaçlar için kullanılabilir. Ayrıca, iki tablo arasındaki eşleşmeyen verilerin belirlenmesine ve düzeltilmesine yardımcı olabilir.
  5. Cross Join: Veritabanındaki iki veya daha fazla tablo arasında herhangi bir ilişki olmaksızın verilerin birleştirilmesini sağlar. Bu join türü, her bir kayıt için diğer tablonun tüm kayıtlarıyla birleştirilmesini sağlar. Yani bir tablo içindeki her bir kayıt diğer tablo içindeki tüm kayıtlarla eşleştirilir. Cross join, verileri çok fazla artırabilir ve performans sorunlarına yol açabilir, bu yüzden performansı önemli olan uygulamalarda sıklıkla kullanılmaz. Ancak veri keşfetme ve analitik uygulamalarda kullanılabilir.
 
*-INNER JOIN*

Aşağıdaki durumlarda inner join kullanılabilir:

- Eşleşen verilerin belirlenmesi: Inner join, iki tablo arasındaki eşleşen verilerin belirlenmesine yardımcı olabilir.
- Verilerin filtrelenmesi: Inner join, verilerin belirli bir kriterle filtrelenmesi gerektiğinde kullanılabilir. Örneğin, belirli bir tarih aralığında yapılan siparişlerin listelenmesi gerektiğinde.
- Verilerin eşleştirilmesi: Inner join, iki tablo arasındaki verilerin eşleştirilmesi gerektiğinde kullanılabilir. Örneğin, müşteri bilgileri ve sipariş bilgilerinin eşleştirilmesi gerektiğinde.
- Verilerin sınırlandırılması: Inner join, verilerin belirli bir kriterle sınırlandırılması gerektiğinde kullanılabilir. Örneğin, belirli bir şehirdeki müşterilerin siparişlerinin listelenmesi gerektiğinde.
 
         SELECT students.student_id, students.name, departments.department

         FROM students

         INNER JOIN departments

         ON students.student_id = departments.student_id;
