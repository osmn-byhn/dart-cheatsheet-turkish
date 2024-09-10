# Giriş:
Tüm Dart Kodları bir `main()` içinde çalışır. Örnek bir kod olarak klasik bir `Hello World` Kodu yazalım.
```
void main() {
    print('Hello World!');
}
```

## Yorum Satırları:
Yorum satırları kod tarafından okunmaz ve derlenmez. Yorum satırları yazılımcının ve ekibinin bazı notlarını veyahut kodu açıklaması için yazılan açıklamaların yazılacağı kısımdır. Yorum satırları **clean code** prensibi ve ekip çalışması için önemli bir faktördür.

- Dart'ta tek satırlık yorum satırları `//` ile başlar. Örneğin;

    ```dart
    // Bu bir tek satırlık Yorum satırıdır
    ```

- Dart'ta çok satırlık yorum satırları `/* */` arasına yazılır. Öncekinden farkı çok satırlı olarak kullanılabilir. Örnek kullanım;

    ```dart
    /*
    Bu bir çok satırlık yorum satırıdır.
    Bu kodlar okunmaz veyahut derlenmez.
    */
    ```

# Syntax Temelleri:
Dart dilinin temel syntax yapısı hakkında bilgi edineceğiz.

## Değişkenler:
Değişkenler, program içerisinde kullanılan ve değişkenlik gösteren değerlerdir. 
- Değişkenler `var`, `final` ve `const` anahtar kelimeleri ile tanımlanabilir.
  - `var` anahtar kelimesi ile tanımlanan değişkenler tipini derleme zamanında otomatik olarak belirler.
    ```dart
    var name = 'Osman';
    ```

  - `final` anahtar kelimesi ile tanımlanan değişkenler, bir kere atanan değerini değiştiremez.
    ```dart
    final surname = 'Beyhan';
    ```

  - `const` anahtar kelimesi ile tanımlanan değişkenler, program çalıştırıldığında sabitlenir ve değiştirilemez.
    ```dart
    const pi = 3.14;
    ```

- Değişkenler tipine göre de tanımlanabilir.
    Dart dilinde çeşitli veri türleri (değişken tipleri) bulunmaktadır. Bu veri tipleri, Dart'ın statik olarak tür kontrolüne dayalı güçlü yapısını destekler. Dart'taki temel değişken tiplerini şu şekilde özetleyebiliriz:

    ### 1. **`int`**
    Tam sayıları temsil eder. Pozitif ve negatif tam sayıları kapsar.
    ```dart
    int age = 30;
    int negative = -5;
    ```

    ### 2. **`double`**
    Ondalıklı sayılar için kullanılır. Kesirli değerler temsil edilir.
    ```dart
    double height = 1.75;
    double pi = 3.14159;
    ```

    ### 3. **`num`**
    Hem `int` hem de `double` türlerini kapsayan bir veri türüdür. `int` ve `double` değerleri alabilir.
    ```dart
    num temperature = 37.5;
    num year = 2024;
    ```

    ### 4. **`String`**
    Metin ifadelerini temsil eder. Tek veya çift tırnakla belirtilir.
    ```dart
    String name = 'Osman Beyhan';
    String greeting = "Merhaba, Dünya!";
    ```

    ### 5. **`bool`**
    Mantıksal veri tipi olup, `true` veya `false` değerlerini alır.
    ```dart
    bool isLoggedIn = true;
    bool isRaining = false;
    ```

    ### 6. **`List`**
    Bir dizi veya listeyi temsil eder. Hem sabit boyutlu hem de dinamik olarak büyüyebilen yapılar oluşturulabilir.
    ```dart
    List<int> numbers = [1, 2, 3, 4];
    List<String> names = ['Ahmet', 'Mehmet', 'Ayşe'];
    ```

    ### 7. **`Set`**
    Her öğesi benzersiz olan ve sıralanmamış koleksiyonları temsil eder.
    ```dart
    Set<int> uniqueNumbers = {1, 2, 3, 4, 5};
    ```

    ### 8. **`Map`**
    Anahtar-değer çiftleri ile çalışan veri yapısıdır.
    ```dart
    Map<String, int> ages = {'Ali': 25, 'Veli': 30};
    ```

    ### 9. **`dynamic`**
    Bir değişkenin veri türünün çalışma zamanında belirlenmesini sağlar. `dynamic` türü kullanıldığında, o değişken herhangi bir veri tipi alabilir.
    ```dart
    dynamic value = 42;
    value = 'Bir metin';  // Türü değiştirebilir.
    ```

    ### 10. **`var`**
    Veri tipini otomatik olarak belirler. Bir kez belirlendikten sonra değişkenin tipi sabit kalır.
    ```dart
    var city = 'Istanbul';  // Dart bunu otomatik olarak String olarak belirler.
    var score = 100;        // Dart bunu int olarak belirler.
    ```

    ### 11. **`Object`**
    Dart'taki tüm nesnelerin üst sınıfıdır. Herhangi bir veri türü `Object` tipinde bir değişkene atanabilir.
    ```dart
    Object something = 'Dart';
    something = 123;
    ```

    ### 12. **`Null`**
    `null` değerini tutabilen bir türdür. Dart'ta, değişkenler varsayılan olarak `null` değer alabilir.
    ```dart
    String? name = null;  // null olabilmesi için '?' işareti ile tanımlanır.
    ```

    Bu veri türleri Dart'ın temelini oluşturur ve daha karmaşık yapılar ve sınıflar tanımlamak için kullanılabilir.


## Operatörler:
Tabii, Dart dilindeki operatörler farklı kategorilere ayrılmaktadır. Bu kategoriler arasında aritmetik, karşılaştırma, mantıksal, bit düzeyinde operatörler ve atama operatörleri gibi gruplar bulunur. 

| Operatör | Açıklama | Örnek |
|----------|----------|-------|
| **Aritmetik Operatörler** | | |
| `+` | Toplama | `a + b` |
| `-` | Çıkarma | `a - b` |
| `*` | Çarpma | `a * b` |
| `/` | Bölme | `a / b` |
| `%` | Mod alma (kalan bulma) | `a % b` |
| `~/` | Tamsayı bölme | `a ~/ b` |
| `++` | Bir artırma (öncesi veya sonrası) | `a++` veya `++a` |
| `--` | Bir azaltma (öncesi veya sonrası) | `a--` veya `--a` |
| **Karşılaştırma Operatörleri** | | |
| `==` | Eşit mi? | `a == b` |
| `!=` | Eşit değil mi? | `a != b` |
| `>` | Büyüktür | `a > b` |
| `<` | Küçüktür | `a < b` |
| `>=` | Büyük veya eşit | `a >= b` |
| `<=` | Küçük veya eşit | `a <= b` |
| **Mantıksal Operatörler** | | |
| `&&` | Mantıksal VE (Logical AND) | `a && b` |
| `||` | Mantıksal VEYA (Logical OR) | `a || b` |
| `!` | Mantıksal DEĞİL (Logical NOT) | `!a` |
| **Bit Düzeyinde Operatörler** | | |
| `&` | Bit düzeyinde VE (AND) | `a & b` |
| `|` | Bit düzeyinde VEYA (OR) | `a | b` |
| `^` | Bit düzeyinde Özel VEYA (XOR) | `a ^ b` |
| `~` | Bit düzeyinde TERSİ (NOT) | `~a` |
| `<<` | Bitleri sola kaydırma | `a << 2` |
| `>>` | Bitleri sağa kaydırma | `a >> 2` |
| **Atama Operatörleri** | | |
| `=` | Atama | `a = b` |
| `+=` | Toplam ve atama | `a += b` |
| `-=` | Fark ve atama | `a -= b` |
| `*=` | Çarpım ve atama | `a *= b` |
| `/=` | Bölüm ve atama | `a /= b` |
| `~/=` | Tamsayı bölüm ve atama | `a ~/= b` |
| `%=` | Kalan ve atama | `a %= b` |
| `&=` | Bit düzeyinde VE ve atama | `a &= b` |
| `|=` | Bit düzeyinde VEYA ve atama | `a |= b` |
| `^=` | Bit düzeyinde XOR ve atama | `a ^= b` |
| `<<=` | Bitleri sola kaydırma ve atama | `a <<= 2` |
| `>>=` | Bitleri sağa kaydırma ve atama | `a >>= 2` |
| **Diğer Operatörler** | | |
| `?.` | Eğer null değilse üye erişimi sağlar | `a?.b` |
| `??` | Null kontrolü (Eğer null ise alternatif değer döner) | `a ?? b` |
| `??=` | Eğer null ise atama | `a ??= b` |
| `is` | Tür kontrolü | `a is String` |
| `is!` | Tür kontrolü (değilse) | `a is! int` |
| `as` | Tür dönüştürme | `a as String` |
| `[]` | Listeden öğe alma | `a[0]` |
| `[]=` | Listeye öğe atama | `a[0] = 5` |
| `()` | Fonksiyon çağırma | `myFunction()` |

### Özel Operatörler Açıklamaları:
- **`?.` (Koşullu Üye Erişimi)**: Eğer bir nesne `null` ise, `?.` operatörü null kontrolü yapar ve üye erişimini engeller.
    ```dart
    String? name;
    print(name?.length);  // null döner
    ```
  
- **`??` (Null Birleşim Operatörü)**: Eğer bir değer `null` ise, alternatif bir değer döner.
    ```dart
    String? name;
    String userName = name ?? 'Guest';
    ```

- **`??=` (Null ile Atama)**: Eğer bir değişken `null` ise, ona bir değer atanır.
    ```dart
    String? name;
    name ??= 'Guest';  // Eğer name null ise 'Guest' atanır.
    ```

Bu operatörler Dart dilinde temel yapı taşlarını oluşturarak, ifadelerin daha kısa ve okunabilir bir şekilde yazılmasına olanak sağlar.

