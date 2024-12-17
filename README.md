# Çözüm
proje/\n
|    |-- Base/
|    |       |-- __init__.py
|    |       |-- BaseClass.py
|    |-- Sub/
|    |       |-- __init__.py
|    |       |-- SubClass.py
|    |-- main.py

yukarıdaki yapıya benzer bir yapım vardı ve bu şekilde iken SubClass.py' den BaseClass.py' deki bir Class' a erişmek için şunu kullanıyordum : **from ..Base.BaseClass import (class'ın ismi)** 
ama bu şekilde kullanınca **"attempted relative import beyond top-level package pythonattempted relative import beyond top-level package python"** hatası verdi.
Bu yapıda kök dizininiz main.py ve anladığım kadarıyla python ancak bu dizinin alt dizinlerini çözümleyebiliyor. Yani siz SubClass'da ".." diyerek üst dizine çıkmak istediğinizde burası çözümlenmediği için
bu dizine erişemiyor.
Ama : 


proje/
|    |-- Base/
|    |       |-- __init__.py
|    |       |-- BaseClass.py
|    |-- Sub/
|    |       |-- __init__.py
|    |       |-- SubClass.py
main.py

Yapınızı buna çevirince, Base ve Sub dosyalarının bulunduğu dizine erişebiliyor ".." işlemi hatasız çalışıyor.(en azından bende öyle oldu)
Ve aynı şekilde **from ..Base.BaseClass import (class'ın ismi)** satırı bu kez hata vermedi.
