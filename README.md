# Phonebook Application

Motoko dilinde yazılmış bir telefon rehberi ve mesaj gönderme uygulaması.

## Projenin Amacı
Bu proje, kullanıcılara bir telefon rehberi oluşturma, giriş ekleme, telefon numarası sorgulama ve mesaj gönderme gibi işlemleri yapma imkanı sunar. Uygulama, `HashMap` veri yapısını kullanarak isim ve telefon bilgilerini depolar ve mesaj geçmişini saklar.

## Kullanılan Teknolojiler
- **Motoko**: Uygulamanın geliştirilmesi için kullanılan dil.
- **Internet Computer**: Kodun çalıştığı ağ.
- **HashMap**: Verilerin organize edilmesi ve depolanması için kullanılan veri yapısı.

## Fonksiyonlar
### 1. Telefon Rehberi Fonksiyonları
- **`insert(name : Name, entry : Entry)`**
  - Bir isim ve telefon numarası ekler.
  - **Parametreler:**
    - `name`: İsim (örneğin, `"John Doe"`)
    - `entry`: Telefon bilgisi ve açıklama içeren bir nesne (örneğin, `{ desc = "Work"; phone = "555-1234" }`).

- **`getPhone(name : Name) -> ?Entry`**
  - Verilen isme ait telefon numarasını sorgular.
  - **Parametre:** `name`: İsim.
  - **Döndürür:** Telefon girişini (eğer varsa).

### 2. Mesajlaşma Fonksiyonları
- **`sendMessage(senderPhone : Phone, message : Message)`**
  - Verilen telefon numarasından bir alıcıya mesaj gönderir.
  - **Parametreler:**
    - `senderPhone`: Gönderici telefon numarası.
    - `message`: Mesaj bilgisi içeren bir nesne (örneğin, `{ receiver = "Jane"; message = "Hello!" }`).

- **`sentMessages(senderPhone : Phone) -> ?Message`**
  - Gönderici telefon numarasına ait mesaj geçmişini getirir.
  - **Parametre:** `senderPhone`: Gönderici telefon numarası.
  - **Döndürür:** Gönderilen mesajları (eğer varsa).

## Örnek Kullanım
### Telefon Rehberi
1. Yeni bir giriş ekleme:
   ```motoko
   let entry = { desc = "Work"; phone = "555-1234" };
   await Phonebook.insert("John Doe", entry);
## Kurulum ve Çalıştırma
1. Kodları Motoko Playground'da çalıştırabilirsiniz: [Motoko Playground]([https://m7sm4-2iaaa-aaaab-qabra-cai.ic0.app/](https://m7sm4-2iaaa-aaaab-qabra-cai.raw.ic0.app/?tag=1214004840))
