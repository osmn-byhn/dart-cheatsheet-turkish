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

## Meta Data:
Dart'ta **metadata**, kodunuza ek açıklamalar veya bilgi eklemek için kullanılır. Metadata, sınıflar, değişkenler, fonksiyonlar, parametreler ve diğer dil öğelerine açıklama ekleyerek onların anlamını genişletmeye ve belirli işlevler eklemeye olanak tanır. Dart'taki metadata'yı genellikle **annotation** (açıklama) olarak adlandırırız.

Metadata, **@** sembolü ile kullanılır ve genellikle bir sınıf ya da const ile tanımlanan bir sabit ile birlikte gelir.

### Yaygın Kullanım Alanları

1. **`@override`**: Bir metodun üst sınıf tarafından tanımlanan bir metodu geçersiz kıldığını belirtir.
2. **`@deprecated`**: Bir sınıf, metod veya özellik artık kullanılmıyorsa, bunun yerine neyin kullanılacağını belirtmek için kullanılır.
3. **Custom (özel) metadata**: Kendi metadata sınıflarınızı oluşturabilir ve kullanabilirsiniz.

### Örnekler

#### 1. `@override` Kullanımı
```dart
class Animal {
  void sound() {
    print('Animal makes a sound');
  }
}

class Dog extends Animal {
  @override
  void sound() {
    print('Dog barks');
  }
}
```
Burada `@override`, `Dog` sınıfının `sound` metodunun `Animal` sınıfındaki aynı isimli metodu geçersiz kıldığını belirtir.

#### 2. `@deprecated` Kullanımı
```dart
class MyClass {
  @deprecated
  void oldMethod() {
    print('This method is deprecated');
  }

  void newMethod() {
    print('This is the new method');
  }
}
```
`@deprecated` ile işaretlenmiş metod, artık kullanılmaması gereken bir metod olduğunu belirtir. Derleyici bu metodu kullanırsanız bir uyarı verecektir.

#### 3. Özel Metadata Oluşturma
Dart'ta kendi metadata'nızı tanımlayabilir ve kullanabilirsiniz. Örneğin, bir sınıfı özel bir işaretle işaretlemek istiyorsanız:

```dart
class MyAnnotation {
  final String info;

  const MyAnnotation(this.info);
}

@MyAnnotation('This is a custom annotation')
class MyClass {
  void myMethod() {
    print('Using custom metadata');
  }
}
```

Burada `MyAnnotation` adında bir metadata tanımlanmış ve `MyClass` üzerine uygulanmıştır. Bu sayede `MyClass`'ın belirli bir bilgiyle işaretlendiği görülür.

### Sonuç

Dart'taki metadata, kodunuza açıklama eklemek, belirsizliği azaltmak veya derleyiciye ve programcıya belirli yönergeler vermek için kullanılır. Hem yerleşik (built-in) hem de özel metadata tanımlayarak kodunuzu daha anlamlı hale getirebilirsiniz.

## Kütüphaneler ve `import` etme:
Dart dilinde **kütüphaneler** (libraries), kodunuzu modüler bir şekilde düzenlemek ve yeniden kullanılabilir hale getirmek için kullanılır. Dart'ta kütüphaneler, genellikle başka projelerde de kullanılabilecek sınıflar, fonksiyonlar ve değişkenler içerir. Bu kütüphaneleri kullanabilmek için kodunuza `import` anahtar kelimesiyle dahil edebilirsiniz.

### Kütüphaneler (Libraries)

Her Dart dosyası aslında bir kütüphane olarak kabul edilir. Ancak, daha karmaşık projelerde kodunuzu daha iyi organize etmek için birden fazla kütüphane oluşturabilirsiniz.

Dart'ta üç ana türde kütüphane bulunur:

1. **Yerleşik Kütüphaneler (Built-in Libraries)**: Dart tarafından sağlanan ve `dart:` ile başlayan kütüphaneler.
2. **Paket Kütüphaneleri (Package Libraries)**: `pub.dev` gibi kaynaklardan gelen ve `package:` ile başlayan kütüphaneler.
3. **Yerel veya Özelleştirilmiş Kütüphaneler**: Projeye özel kütüphaneler.

### `import` Kullanımı

Dart'ta bir kütüphaneyi kullanmak için `import` anahtar kelimesi kullanılır. Kütüphaneler şu formatlarda import edilir:

1. **Yerleşik Kütüphaneler (dart:)**
2. **Paket Kütüphaneleri (package:)**
3. **Dosya Yolu ile Kütüphaneler**

#### 1. Yerleşik Kütüphaneler (`dart:`)

Dart diliyle birlikte gelen yerleşik kütüphaneler `dart:` ile başlar. Örneğin:
```dart
import 'dart:math';  // Matematiksel fonksiyonlar için
import 'dart:io';    // I/O işlemleri için
import 'dart:convert'; // JSON ve UTF-8 işlemleri için
```

#### 2. Paket Kütüphaneleri (`package:`)

Dart'ın `pub.dev` paket yöneticisiyle indirilen kütüphaneler `package:` ile kullanılır. Örneğin, `http` paketini kullanarak HTTP istekleri yapabilirsiniz:
```dart
import 'package:http/http.dart' as http;  // HTTP istekleri için
```

`pubspec.yaml` dosyanızda bu paketleri belirtmeniz gerektiğini unutmayın:
```yaml
dependencies:
  http: ^0.13.3
```

#### 3. Yerel Dosya Yolu ile Kütüphaneler

Kendi projenizdeki başka bir dosyadan kütüphane import etmek için dosya yolunu kullanabilirsiniz:
```dart
import 'lib/my_library.dart'; // Projedeki bir dosyayı import eder
```

### `import` Seçenekleri

Dart'ta kütüphanelerle çalışırken bazı ek özellikler kullanabilirsiniz:

#### 1. `as`: Bir Kütüphaneye Takma Ad Vermek
Bir kütüphaneyi import ederken ona bir takma ad verebilirsiniz. Bu özellikle aynı isimde fonksiyon veya sınıflar olduğunda çakışmaları önlemek için kullanılır.
```dart
import 'package:http/http.dart' as http;
import 'package:my_project/network.dart' as network;

void main() {
  http.get(...);
  network.request(...);
}
```

#### 2. `show`: Belirli Fonksiyonları veya Sınıfları İçe Aktarmak
Bir kütüphaneden sadece belirli elemanları almak için `show` kullanabilirsiniz:
```dart
import 'dart:math' show pi, sqrt;  // Sadece pi ve sqrt fonksiyonlarını import eder
```

#### 3. `hide`: Belirli Fonksiyonları veya Sınıfları Gizlemek
Bir kütüphaneden bazı elemanları gizlemek için `hide` kullanabilirsiniz:
```dart
import 'dart:math' hide sin, cos;  // sin ve cos fonksiyonlarını gizler, diğerlerini import eder
```

#### 4. `deferred as`: Gecikmeli Yükleme
Eğer büyük bir kütüphaneyi ihtiyaç duyulana kadar yüklemek istemiyorsanız, gecikmeli yükleme kullanabilirsiniz. Bu, performans optimizasyonu sağlar.
```dart
import 'package:my_library/my_library.dart' deferred as myLibrary;

void main() async {
  await myLibrary.loadLibrary();  // Kütüphaneyi yükler
  myLibrary.someFunction();
}
```

### Örnekler

#### Örnek: Yerleşik Kütüphaneyi Kullanma
```dart
import 'dart:math';

void main() {
  var random = Random();
  print(random.nextInt(100)); // 0 ile 100 arasında rastgele sayı üretir
}
```

#### Örnek: Paket Kütüphanesini Kullanma
```dart
import 'package:http/http.dart' as http;

void main() async {
  var response = await http.get(Uri.parse('https://example.com'));
  print('Response status: ${response.statusCode}');
  print('Response body: ${response.body}');
}
```

## Anahtar Kelimeler (Keywords):
Dart'ta **anahtar kelimeler** (keywords), dilin yapısal öğelerini ifade eden, özel anlamlara sahip kelimelerdir. Bu kelimeler, programda belirli işlemleri gerçekleştirmek ve dilin kurallarını tanımlamak için kullanılır. Dart dilinde, bu kelimeler değişken, fonksiyon, sınıf adı vb. olarak kullanılamaz.

Aşağıda Dart dilinde kullanılan tüm anahtar kelimeler:

| `abstract` | `else`     | `import`  | `super`  | `as`      | `enum`     |
|------------|------------|-----------|----------|-----------|------------|
| `assert`   | `export`   | `in`      | `switch` | `async`   | `extends`  |
| `await`    | `external` | `is`      | `sync`   | `break`   | `factory`  |
| `case`     | `false`    | `mixin`   | `this`   | `catch`   | `final`    |
| `class`    | `finally`  | `new`     | `throw`  | `const`   | `for`      |
| `continue` | `Function` | `null`    | `true`   | `covariant` | `get`    |
| `default`  | `if`       | `on`      | `typedef`| `deferred` | `implements` |
| `do`       | `interface`| `operator`| `var`    | `dynamic` | `in`       |
| `else`     | `extends`  | `part`    | `void`   | `enum`    | `with`     |

# Tipler ve Methodları:
Dart dilinde çeşitli veri türleri ve tip sistemleri bulunur. Aşağıda, Dart'taki ana veri türleri ve tip sistemleri hakkında detaylı bilgi verilmiş ve her biri için kullanılabilecek methodlar ve fonksiyonlar tablo şeklinde sunulmuştur.

### 1. **Built-in Types (Yerleşik Tipler)**

| Veri Tipi     | Method/Fonksiyon                  | Açıklama                                                                           | Örnek                                                                                 |
|---------------|-----------------------------------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| **int**       | `abs()`                           | Sayının mutlak değerini döndürür.                                                   | `(-5).abs()` -> `5`                                                                   |
|               | `compareTo()`                     | İki sayıyı karşılaştırır. (Küçükse -1, eşitse 0, büyükse 1 döner.)                  | `5.compareTo(3)` -> `1`                                                               |
|               | `isEven`                          | Sayının çift olup olmadığını kontrol eder.                                          | `4.isEven` -> `true`                                                                  |
|               | `isOdd`                           | Sayının tek olup olmadığını kontrol eder.                                           | `3.isOdd` -> `true`                                                                   |
| **double**    | `ceil()`                          | Sayıyı yukarı yuvarlar.                                                             | `2.3.ceil()` -> `3`                                                                   |
|               | `floor()`                         | Sayıyı aşağı yuvarlar.                                                              | `2.9.floor()` -> `2`                                                                  |
|               | `round()`                         | Sayıyı en yakın tam sayıya yuvarlar.                                                | `3.14.round()` -> `3`                                                                 |
|               | `toInt()`                         | Ondalık sayıyı tam sayıya çevirir.                                                  | `3.99.toInt()` -> `3`                                                                 |
| **String**    | `contains()`                      | Metnin belirli bir alt diziyi içerip içermediğini kontrol eder.                     | `"dart".contains('ar')` -> `true`                                                     |
|               | `length`                          | Metin uzunluğunu döner.                                                            | `"Hello".length` -> `5`                                                               |
|               | `toLowerCase()`                   | Metni küçük harfe çevirir.                                                          | `"DART".toLowerCase()` -> `"dart"`                                                    |
|               | `toUpperCase()`                   | Metni büyük harfe çevirir.                                                          | `"dart".toUpperCase()` -> `"DART"`                                                    |
|               | `substring()`                     | Metnin belirli bir kısmını alır.                                                    | `"dart".substring(1, 3)` -> `"ar"`                                                    |
| **bool**      | `toString()`                      | Mantıksal değeri (true/false) string olarak döndürür.                               | `true.toString()` -> `"true"`                                                         |
| **List**      | `add()`                           | Listeye bir eleman ekler.                                                          | `list.add(10)`                                                                        |
|               | `remove()`                        | Listeden bir eleman siler.                                                          | `list.remove(10)`                                                                     |
|               | `length`                          | Listenin uzunluğunu döner.                                                         | `[1, 2, 3].length` -> `3`                                                             |
|               | `contains()`                      | Listenin bir elemanı içerip içermediğini kontrol eder.                              | `[1, 2, 3].contains(2)` -> `true`                                                     |
|               | `join()`                          | Listedeki öğeleri birleştirir ve bir string döner.                                  | `["a", "b", "c"].join(",")` -> `"a,b,c"`                                              |
| **Set**       | `add()`                           | Set'e bir eleman ekler.                                                            | `set.add(4)`                                                                          |
|               | `remove()`                        | Set'ten bir eleman siler.                                                          | `set.remove(3)`                                                                       |
|               | `contains()`                      | Set'in bir elemanı içerip içermediğini kontrol eder.                                | `{1, 2, 3}.contains(2)` -> `true`                                                     |
| **Map**       | `addAll()`                        | Birden fazla anahtar-değer çifti ekler.                                             | `map.addAll({"key2": 2, "key3": 3})`                                                  |
|               | `remove()`                        | Belirli bir anahtar-değer çiftini siler.                                            | `map.remove("key1")`                                                                  |
|               | `containsKey()`                   | Haritanın belirli bir anahtarı içerip içermediğini kontrol eder.                    | `map.containsKey("key1")` -> `true`                                                   |
|               | `containsValue()`                 | Haritanın belirli bir değeri içerip içermediğini kontrol eder.                      | `map.containsValue(1)` -> `true`                                                      |

### 2. **Records (Kayıtlar)**

| Özellik | Method/Fonksiyon | Açıklama | Örnek |
|---------|------------------|----------|-------|
| **Kayıt Tanımlama** | - | Record'lar, adlandırılmış alanlar içeren veri yapılarıdır. | `var person = (name: 'Osman', age: 30);` |
| **Alan Erişimi** | - | Alanlara `.` (nokta) operatörü ile erişilir. | `print(person.name); // Çıktı: Osman` |
| **Yeniden Tanımlama** | `with` | Alanları değiştirerek yeni kayıt oluşturma. | `var updatedPerson = person with (age: 31);` |
| **Destructuring** | - | İçerikleri ayırmak için destructuring kullanılır. | `var (name, age) = person;` |
| **`toString()`** | `toString()` | Record'un string temsilini döndürür. | `print(person.toString()); // Çıktı: (name: Osman, age: 30)` |
| **`hashCode`** | `hashCode` | Record'un hash kodunu döndürür. | `print(person.hashCode); // Çıktı: Bir sayısal hash kodu` |
| **`runtimeType`** | `runtimeType` | Record'un türünü döndürür. | `print(person.runtimeType); // Çıktı: (name: String, age: int)` |

### 3. **Collections (Koleksiyonlar)**

#### **List**

| Method/Fonksiyon | Açıklama | Örnek |
|------------------|----------|-------|
| `add()` | Listeye bir eleman ekler. | `list.add(10)` |
| `remove()` | Listeden bir eleman siler. | `list.remove(10)` |
| `length` | Listenin uzunluğunu döner. | `[1, 2, 3].length` -> `3` |
| `contains()` | Liste içinde bir eleman olup olmadığını kontrol eder. | `[1, 2, 3].contains(2)` -> `true` |
| `join()` | Liste öğelerini birleştirir ve string döner. | `["a", "b", "c"].join(",")` -> `"a,b,c"` |
| `sort()` | Listeyi sıralar. | `list.sort()` |

#### **Set**

| Method/Fonksiyon | Açıklama | Örnek |
|------------------|----------|-------|
| `add()` | Set'e bir eleman ekler. | `set.add(4)` |
| `remove()` | Set'ten bir eleman siler. | `set.remove(3)` |
| `contains()` | Set'in bir elemanı içerip içermediğini kontrol eder. | `{1, 2, 3}.contains(2)` -> `true` |
| `union()` | İki setin birleşimini döndürür. | `{1, 2}.union({2, 3})` -> `{1, 2, 3}` |
| `intersection()` | İki setin kesişimini döndürür. | `{1, 2}.intersection({2, 3})` -> `{2}` |

#### **Map**

| Method/Fonksiyon | Açıklama | Örnek |
|------------------|----------|-------|
| `addAll()` | Birden fazla anahtar-değer çifti ekler. | `map.addAll({"key2": 2, "key3": 3})` |
| `remove()` | Belirli bir anahtar-değer çiftini siler. | `map.remove("key1")` |
| `containsKey()` | Belirli bir anahtarı içerip içermediğini kontrol eder. | `map.containsKey("key1")` -> `true` |
| `containsValue()` | Belirli bir değeri içerip içermediğini kontrol eder. | `map.containsValue(1)` -> `true` |
| `forEach()` | Map'teki her anahtar-değer çifti için bir işlem yapar. | `map.forEach((key, value) => print('$key: $value'));` |

### 4. **Generics (Genel Türler)**

| Özellik | Method/Fonksiyon | Açıklama | Örnek |
|---------|------------------|----------|-------|
| **Genel Listeler** | `add()` | Liste

ye eleman ekler. | `List<int> numbers = []; numbers.add(1);` |
| **Genel Mapler** | `putIfAbsent()` | Anahtar mevcut değilse yeni anahtar-değer çifti ekler. | `Map<String, int> map = {}; map.putIfAbsent('key', () => 1);` |
| **Genel Fonksiyonlar** | `Function<T>` | Tip güvenli fonksiyonları temsil eder. | `Function<int> square = (int x) => x * x;` |
| **Kapsayıcı Sınıflar** | `T` | Genel türler içeren sınıflar. | `class Box<T> { T value; Box(this.value); }` |

### 5. **Typedefs (Tür Tanımları)**

| Özellik | Method/Fonksiyon | Açıklama | Örnek |
|---------|------------------|----------|-------|
| **Fonksiyon Tipi Tanımlama** | `typedef` | Fonksiyon türlerini tanımlar. | `typedef IntFunction = int Function(int);` |
| **Kullanım** | - | Tanımlanan tipi bir fonksiyon olarak kullanma. | `IntFunction addOne = (int x) => x + 1;` |

### 6. **Type System (Tür Sistemi)**

| Özellik | Method/Fonksiyon | Açıklama | Örnek |
|---------|------------------|----------|-------|
| **Dinamik Tür** | `dynamic` | Her türde değer alabilen bir değişken türüdür. | `dynamic x = 10; x = 'string';` |
| **Nötr Tür** | `Object` | Tüm Dart nesnelerinin temel türüdür. | `Object obj = 'hello'; obj = 42;` |
| **Sabit Türler** | `const` | Sabit değerleri temsil eder. | `const pi = 3.14;` |
| **Final** | `final` | Bir kere atandıktan sonra değişmeyen değişkenler. | `final name = 'Osman';` |


