# Introduce<br>
## 中文<br>
SimpleSearch 是一款极简风格的搜索主页，其功能仅限于搜索，无其他任何附加功能。<br>
该主页纯由 Html 代码构建而成，并无后端支持。<br>
用户可在 Vercel、Zeabur 等服务平台上部署本项目，并可根据自身需求增添更多内容。具体操作方式为：首先 Fork 本项目，然后选择从 Github 仓库进行部署。这一过程极为简便。<br>
## English<br>
SimpleSearch is a minimalist search homepage that is limited to search and nothing else.<br>
The homepage is built purely from Html code and has no backend support.<br>
Users can deploy this project on Vercel, Zeabur and other service platforms, and add more content according to their needs. To do this, first Fork the project and then choose to deploy from a Github repository. The process is extremely easy.<br>
## 日本語<br>
SimpleSearchは、検索だけに特化したミニマルな検索ホームページです。<br>
このホームページは純粋にHTMLコードだけで作られており、バックエンドのサポートはありません。<br>
ユーザーはこのプロジェクトをVercel、Zeabur、その他のサービスプラットフォームにデプロイし、必要に応じてコンテンツを追加することができます。 これを行うには、まずプロジェクトをフォークし、Githubリポジトリからのデプロイを選択する。 プロセスは非常に簡単だ。<br>
——————————<br>
![屏幕截图_21-7-2024_23027_simplesearch rth10 com](https://github.com/user-attachments/assets/4ecd1e82-26d8-4166-ab23-daab70485953)
# Code interpretation<br>
## 中文
**HTML 结构部分**
- `<!DOCTYPE html>`：声明这是一个 HTML5 文档。
- `<html lang="en">`：整个 HTML 文档的开始标签，`lang="en"`表示文档的默认语言是英语。
- `<head>`：包含文档的元数据。
- `<meta charset="UTF - 8">`：设置文档的字符编码为 UTF - 8。
- `<meta name="viewport" content="width=device - width, initial - scale=1.0">`：设置视口，使页面在移动设备上能够正确缩放。
- `<title>Search Page</title>`：定义浏览器标签页上显示的页面标题。
- `<link rel="icon" href="...">`：指定浏览器标签页上显示的图标。
- `<style>`：定义了页面的样式，使用 CSS 样式规则。
- `body`：设置整个页面主体的样式，包括布局（flex 布局）、高度（占满视口高度）、外边距、字体、背景（渐变背景）等。
- `.search - container`：搜索框容器的样式，如文本对齐方式、背景颜色、内边距、边框半径、阴影等。
- `.time`：显示时间的元素样式。
- `.logo`：页面 logo 的样式，包括字体大小、粗细、颜色、背景颜色、内边距、边框半径、过渡效果等。
- `.search - container h1`：搜索框容器内标题的样式。
- `.search - box`：搜索框的整体样式。
- `.search - box input[type="text"]`：搜索输入框的样式，如宽度、内边距、边框、边框半径、轮廓、字体大小、过渡效果等。
- `.search - box button`：搜索按钮的样式，如内边距、边框、背景颜色、颜色、字体大小、光标样式、过渡效果等。
- `.footer`：页脚的样式。
- `.search - engine`：搜索引擎选择下拉框的样式。
- `.settings - button`：设置按钮的样式。
- `.settings - dropdown`：设置下拉菜单的样式。
- `<script>`：包含了页面的 JavaScript 代码。

**JavaScript 部分**
- `const translations`：定义了一个包含多种语言（英语、中文、日语）翻译文本的对象，用于实现多语言切换。
- `setLanguage(lang)`：根据传入的语言代码`lang`，更新页面上各个元素的文本内容为相应语言的翻译文本，同时更新语言选择下拉框的选项，并将选择的语言保存到本地存储`localStorage`中。
- `setSearchEngine(form)`：根据用户选择的搜索引擎和输入的查询内容，构建相应搜索引擎的搜索链接，并跳转到该链接。
- `toggleSettings()`：切换设置下拉菜单的显示和隐藏状态。
- `updateTime()`：获取当前时间，并将其格式化为本地时间字符串后更新到页面上的时间显示元素中。
- `document.addEventListener("DOMContentLoaded", () => {...})`：在页面加载完成后执行以下操作：
- 为语言选择下拉框添加`change`事件监听器，当选择语言改变时调用`setLanguage`函数。
- 为设置按钮添加点击事件监听器，点击时调用`toggleSettings`函数。
- 从本地存储中获取用户之前选择的首选语言，如果没有则默认使用英语，然后调用`setLanguage`函数设置页面语言。
- 调用`updateTime`函数更新时间，并使用`setInterval`每秒更新一次时间。

**其他脚本部分**
- `(function() {...})();`：这是一个自执行函数，用于向页面添加百度统计脚本。
- `<script charset="UTF - 8" id="LA_COLLECT" src="//sdk.51.la/js - sdk - pro.min.js?id=3IkShiWZpUnnmEBc&ck=3IkShiWZpUnnmEBc&autoTrack=true"></script>`：可能是另一个用于数据收集或分析的第三方脚本。

**页面主体部分（`<body>`）**
- `<div class="settings - button">`：包含设置按钮和设置下拉菜单。
- `<div class="search - container">`：搜索框容器，包含时间显示组件、logo、标题、搜索引擎选择下拉框、搜索框（输入框和搜索按钮）、页脚等元素。
## English
**HTML structure **
- '<! DOCTYPE html> ': Declares that this is an HTML5 document.
- '<html lang="en">' : The opening tag of the entire HTML document, with 'lang="en"' indicating that the default language of the document is English.
- '<head>' : Contains metadata about the document.
- '<meta charset=" UTF-8 ">' : Sets the character encoding of the document to UTF-8.
- '<meta name="viewport" content="width= device-width, initial-scale =1.0">' : Sets the viewport so that the page scales correctly on mobile devices.
- '<title>Search Page</title>' : Defines the page title displayed on the browser TAB.
- `<link rel="icon" href="..." > ': Specifies the icon to display on the browser TAB.
- '<style>' : This defines the style of the page, using CSS rules.
- 'body' : Styles the entire body of the page, including layout (flex layout), height (full viewport height), margins, fonts, background (gradient background), etc.
- '. Search-container ': Styles for the search box container such as text alignment, background color, padding, border radius, shadow, etc.
- '.time ': An element style that displays the time.
- '.logo ': The style of the page's logo, including font size, weight, color, background color, padding, border radius, transition effects, etc.
- '. Search-container h1 ': Styles for the heading inside the search box container.
- '. Search-box ': The overall styling of the search box.
- '. Search-box input[type="text"] ': Styles for the search input such as width, padding, border, border radius, outline, font size, transition, etc.
- '. Search-box button ': search button styles such as padding, border, background color, color, font size, cursor style, transition effects, etc.
- '.footer ': Footer style.
- '. Search-engine ': Styles for the search engine to select drop-down boxes.
- '. settings-button ': Sets the style of the button.
- '. settings-dropdown ': Sets the style of the dropdown menu.
- '<script>' : This contains the JavaScript code of the page.

**JavaScript part **
- 'const translations' : Defines an object containing translations of text in multiple languages (English, Chinese, Japanese).
- 'setLanguage(lang)' : Based on the language code 'lang', update the text content of each element on the page to the translation text of the corresponding language, update the language selection dropdown options, and save the selected language to the 'localStorage'.
- 'setSearchEngine(form)' : Based on the search engine selected by the user and the query entered, build a search link to the corresponding search engine and jump to that link.
- 'toggleSettings()' : Toggles the shown and hidden states of the Settings dropdown.
- 'updateTime()' : Gets the current time, formats it as a local time string and updates it to the time display element on the page.
- `document.addEventListener("DOMContentLoaded", () => {... }) ': when the page is loaded, do the following:
- Add a 'change' event listener to the language selection drop-down and call the 'setLanguage' function when the language selection changes.
- Add a click event listener to the Settings button and call the 'toggleSettings' function when clicked.
- Get the user's previously selected preferred language from local storage, default to English if it's not available, then call the 'setLanguage' function to set the page language.
- Call the 'updateTime' function to update the time and use the 'setInterval' to update the time every second.

** Other scripts **
- `(function() {... }) (); ': This is a self-executing function to add a Baidu stats script to the page.
- `<script charset="UTF - 8" id="LA_COLLECT" src="//sdk.51.la/js - sdk - pro.min.js? id=3IkShiWZpUnnmEBc&ck=3IkShiWZpUnnmEBc&autoTrack=true"></script> ': Could be another third-party script for data collection or analysis.

** The main part of the page (' <body> ') **
- '<div class=" settings-button ">' : Contains the settings button and Settings drop-down menu.
- '<div class=" search-container ">' : The search box container, which contains the time display component, logo, title, search engine selection dropdown, search box (input and search button), footer, etc.
## 日本語
**HTMLの構造部分です**
- `<です!DOCTYPE html>`:これはHTML5のドキュメントです。
- `<html lang="en">`: html文書全体の開始タグです。`lang="en"`は文書のデフォルト言語が英語であることを示します。
- `<head>`:ドキュメントのメタデータを含みます。
- `<meta charset=" utf-8 ">`:文書の文字コードをutf-8に設定します。
- `<meta name="viewport" content="width= device-width, initial-scale =1.0">`:モバイル機器でページが正確にスケーリングできるようにビューポイントを設定します。
- `<title>Search Page</title>`:ブラウザのタブに表示されるページのタイトルを定義します。
- `<link rel="icon" href="…"です>`:ブラウザのタブに表示されるアイコンを指定します。
- `<style>`: CSSスタイルルールを使用してページのスタイルを定義します。
- `body`:レイアウト(flexレイアウト)、高さ(視野いっぱいの高さ)、アウトライン、フォント、背景(グラデーション背景)など、ページ全体のスタイルを設定します。
- `.search - container`:テキストの配置、背景の色、内辺距離、枠半径、陰影など、ボックスの形を検索します。
- `.time`:時間を表示する要素のパターンです。
- `.ロゴ`:ページロゴのスタイルには、フォントの大きさ、太さ、色、背景色、内辺距離、枠半径、遷移効果などがあります。
- `.search - container h1`:ボックス内のタイトルのスタイルを検索します。
- `.search - box`:検索ボックスの全体的なスタイルです。
- `.search - box input[type="text"]`:幅、内辺距離、枠、枠半径、輪郭、フォントサイズ、遷移効果など、入力ボックスのスタイルを検索します。
- `.search - box button`:内辺距離、枠、背景色、色、フォントサイズ、カーソルの形、遷移効果などを検索します。
- `.footer`:フッターのパターンです。
- `. search-engine:検索エンジンはプルダウンを選択します。
- `. settings-button `:設定ボタンの仕様です。
- `. settings-dropdown `:プルダウンメニューを設定します。
- `<script>`:ページのJavaScriptコードを含んでいます。

**JavaScriptの部分です**
- `const translations`:複数の言語(英語、中国語、日本語)の翻訳テキストを含むオブジェクトを定義しています。
- `setLanguage(lang)`:入ってきた言語コード`lang`に従って、ページ上の各要素のテキスト内容を当該言語の翻訳テキストに更新します。同時に、言語選択のプルダウンを更新し、選択した言語をローカルストレージ`localStorage`に保存します。
- `setSearchEngine(form)`:ユーザーが選択した検索エンジンと入力したクエリに基づいて、該当する検索エンジンの検索リンクを構築し、そこにジャンプします。
- `toggleSettings()`:プルダウンメニューの表示と非表示設定を切り替えます。
- `updateTime()`:現在の時間を取得し、ローカルな時間文字列としてフォーマットしてページ上の時間表示要素に更新します。
- ` document . addeventlistener (" domcontentloaded、()= >{…})`:ページの読み込み完了後に以下の操作を実行します。
-言語選択プルダウンボックスに`change`イベントファインダーを追加し、言語の変更を選択すると`setLanguage`関数を呼び出します。
-ボタンを設定するためにイベントの傍受器をクリックして、クリックする時`toggleSettings`関数を呼び出します。
-ローカルストレージからユーザーが選択した最初の選択言語を取得し、ない場合はデフォルトで英語を使用します。そして、「setLanguage」関数を呼び出してページ言語を設定します。
- " updateTime "関数を呼び出して時間を更新し、" setInterval "を使用して1秒間に1回時間を更新します。

**その他スクリプト部分**です
- `(function(){…です})();です`:これは百度の統計シナリオをページに追加するための自己実行関数です。
- `<script charset=" utf-8 " id=" la _ collect " src="//sdk.51.la/js - sdk - pro.min.js?id=3IkShiWZpUnnmEBc&ck=3IkShiWZpUnnmEBc&autoTrack=true"></script>`:データ収集や分析のためのサードパーティのスクリプトかもしれません。

**ページ本体部分(`<body>`) **です。
- `<div class=" settings-button ">`:設定ボタンと設定プルダウンメニューが含まれています。
- `<div class="search - container">`:時間表示コンポーネント、ロゴ、タイトル、検索エンジン選択のためのプルダウン、検索ボックス(入力ボックスと検索ボタン)、ページなどの要素が含まれています。
