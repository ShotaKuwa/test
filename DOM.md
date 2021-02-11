DOM(Document Object Model)  
javascriptでhtml要素を操作するための仕組み  
HTMLやXML文書のためのプログラミングインターフェース  
→HTML(XML)をオブジェクトとして扱い、それを操作する  

1. Tree structure  
html head body header mainとかのコンテンツ  
2. Node  
ノード 子ノード 親ノード 兄弟姉妹ノード  
3. WebページとJavascriptなどのプログラミング言語とを繋ぐ  
API = DOM + JavaScript?  
## DOMで何ができるのか  
 - javascriptを使ってHTMLの情報を取得・変更・イベントの登録などができる  
1. HTML情報を全て取得する  
 - document  
 - headタグやbodyタグなど  
 ex)document.body  
 - bodyタグ内の要素
 ex)document.body.children  
2. 要素取得のメソッド  
 - querySelector  
 ex)document.querySelector()  
 ex)document.querySelector('h1')など  
 HTML内のタグ、id、classなどを指定することができる  　
 上から探して最初に見つかった要素ひとつを取得する  
 - querySelectorALL
 ex)document.querySelectorAll()  
指定した要素全てを取得  
3. 要素にアクセスして変更を加える  
- innerHTML  
要素の中身にアクセスすることが可能  
ex)const h1 = document.querySelector('h1')  
→undefined  
h1.innerHTML  
→"何か中身"  
hi.innerHTML = "書き換えた"  
→"書き換えた"  
innerHTMLはタグを認識する
h1.innerHTML = "書き換えた<span style ='color:red'>かもね＜/span>"  
- textConetent  
要素の中身にアクセスするが、これはタグなどを無視したテキスト情報のみにアクセスする(上記のspanタグは無視される)  
- style  
要素のスタイルにアクセスし、変更できる  
ul.style.color = 'green'  
→'green'  
- 複数要素を取得した場合  
querySelectorAll