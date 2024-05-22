(English text is below)
Adım 1: Ortam Kurulumu

Confluent Kafka'nın Kurulması: Confluent Kafka'yı SASL_SSL, kullanıcı adı, şifre ve önyükleyici sunucular gibi uygun güvenlik ayarlarıyla yapılandırın.
MongoDB Atlas'ın Kurulması: MongoDB Atlas hesabı oluşturun ve bir MongoDB kümesi kurun. Kümelere erişmek için bağlantı dizesini edinin.
Colab'da PySpark ile Spark'ın Kurulması: Apache Spark'ı yükleyin ve Google Colab ortamında PySpark'ı yapılandırın.
Adım 2: URL'den Veri Alınması ve Kafka'ya Gönderilmesi

URL'den Veri Alınması: Python'un requests kütüphanesini kullanarak sağlanan URL'den veriyi alın.
Confluent Kafka Producer'ının Yapılandırılması: Uygun güvenlik ayarlarıyla bir Kafka Producer'ı oluşturun ve yapılandırın.
Verinin Kafka'ya Gönderilmesi: Alınan veriyi Kafka Producer aracılığıyla bir Kafka konusuna gönderin. Benzersizliği sağlamak için URL'yi mesaj anahtarı olarak kullanın.
Adım 3: Kafkadan Veri Tüketilmesi ve MongoDB'ye Kaydedilmesi

Kafka Consumer'ın Kurulması: Kafkadan gelen verileri almak için bir Kafka Consumer yapılandırın ve ilgili Kafka konusuna abone edin.
Mesajların İşlenmesi: Kafka konusundan gelen mesajları alın ve mesaj verisini çözün.
Verinin MongoDB'ye Eklenmesi: MongoDB Atlas kümesine bir bağlantı kurun. Çözülen veriyi, başlangıçta 0 olarak ayarlanmış bir durum bayrağıyla birlikte ekleyin.
Adım 4: Verinin MongoDB'den Çekilerek Düzenlenmesi ve Spark ile Dönüştürülmesi

Verinin MongoDB'den Çekilmesi: MongoDB'den veri çekmek için PyMongo kütüphanesini kullanın.
Verinin Düzenlenmesi: Çekilen veriyi işlemek ve düzenlemek için gerekli dönüşümleri yapın, gerektiğinde veriyi temizleyin ve ön işlemler uygulayın.
Spark ile Dönüştürme: Düzenlenmiş veriyi Spark DataFrame'e dönüştürün ve istenen analizleri veya işlemleri gerçekleştirmek için gerekli Spark işlemlerini uygulayın.
Adım 5: Verinin Makine Öğrenmesi ile Sınıflandırılması

Makine Öğrenmesi Modelinin Eğitilmesi ve Uygulanması: Veriyi makine öğrenmesi algoritmalarıyla işleyin. Özellikle, veriyi k-NN (k-en yakın komşu) algoritması ile sınıflandırarak farklı kategorilere ayırın. Bu, haberlerin belirli kategorilere veya sınıflara doğru bir şekilde yerleştirilmesini sağlar.
Step 1: Environment Setup

Setting Up Confluent Kafka: Configure Confluent Kafka with appropriate security settings such as SASL_SSL, username, password, and bootstrap servers.
Setting Up MongoDB Atlas: Create a MongoDB Atlas account and set up a MongoDB cluster. Obtain the connection string to access the clusters.
Installing Spark with PySpark on Colab: Install Apache Spark and configure PySpark in the Google Colab environment.
Step 2: Fetching Data from URL and Sending to Kafka

Fetching Data from URL: Retrieve data from the provided URL using Python's requests library.
Configuring Confluent Kafka Producer: Create and configure a Kafka Producer with appropriate security settings.
Sending Data to Kafka: Send the retrieved data to a Kafka topic via a Kafka Producer. Use the URL as the message key to ensure uniqueness.
Step 3: Consuming Data from Kafka and Saving to MongoDB

Setting Up Kafka Consumer: Configure a Kafka Consumer to receive data from Kafka and subscribe to the relevant Kafka topic.
Processing Messages: Receive messages from the Kafka topic and decode the message data.
Adding Data to MongoDB: Establish a connection to the MongoDB Atlas cluster. Add the decoded data to the MongoDB cluster along with a status flag initially set to 0.
Step 4: Retrieving and Transforming Data from MongoDB with Spark

Retrieving Data from MongoDB: Use the PyMongo library to retrieve data from MongoDB.
Data Transformation: Process and transform the retrieved data, perform necessary transformations, clean the data if required, and apply preprocessing.
Transformation with Spark: Convert the processed data to a Spark DataFrame and apply required Spark operations for desired analytics or processing.
Step 5: Classifying Data with Machine Learning

Training and Applying Machine Learning Model: Process the data using machine learning algorithms. Specifically, classify the data using the k-NN (k-nearest neighbors) algorithm to categorize the news articles into different classes, ensuring accurate classification of the articles into appropriate categories.





