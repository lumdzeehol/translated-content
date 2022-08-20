---
title: Firefox 4 for developers
slug: Mozilla/Firefox/Releases/4
tags:
  - CSS
  - Firefox
  - Firefox 4
  - Gecko
  - Gecko 2.0
  - HTML
  - JavaScript
  - XPCOM
  - XUL
  - 要更新
translation_of: Mozilla/Firefox/Releases/4
---
<p>Firefox 4 （6 月後半にベータ版リリースが予定されています）では、パフォーマンスが向上し、 HTML 5 やその他の革新的な Web 技術のさらなるサポートが追加され、さらには、セキュリティも改善しています。 この記事では、この次期リリースについてのとっかかりの情報と、 Web 開発者、アドオン開発者、そして、Gecko プラットフォーム開発者向けに利用可能になる機能の一覧を提供します。</p>

<p>これらの機能の多くはすでに <a href="http://www.mozilla.com/en-US/firefox/beta/">Firefox 4 beta</a> リリース、もしくは（冒険心にあふれているなら）<a href="http://nightly.mozilla.org/">ナイトリー trunk ビルド</a> で試すことできます。</p>

<div class="note"><strong>註：</strong>この記事は作成中であり、このページからリンクされている記事もまた同様です。多くの記事名が仮名であり、いくつかのトピックは複数の記事に分割されるかもしれません。</div>

<h2 id="Features_for_web_developers" name="Features_for_web_developers">Web 開発者向け機能</h2>

<p>Gecko は現在 <a href="/ja/docs/HTML/HTML5">HTML5</a> パーサーを利用しています。それはバグが修正され、相互運用性が改善され、また、パフォーマンスが向上されたものです。また、HTML マークアップでコンテンツに <a href="/ja/docs/SVG">SVG</a> と <a href="/ja/docs/MathML">MathML</a> を直接埋め込むことも可能にします。</p>

<h3 id="HTML" name="HTML">HTML</h3>

<dl>
 <dt><a href="/ja/docs/HTML/HTML5/HTML5_Parser">HTML5 パーサー入門</a></dt>
 <dd>HTML5 パーサーが意味することと、どのように SVG と MathML をコンテンツにインラインで埋め込むかの概説。</dd>
 <dt><a href="/ja/docs/HTML/HTML5/Forms_in_HTML5">HTML5 におけるフォーム</a></dt>
 <dd>HTML5 における Web フォームの改善の概説。これらの変更点には <a href="/ja/docs/Web/HTML/Element/input" title="HTML の &lt;input> 要素は、ユーザーからデータを受け取るための、ウェブベースのフォーム用の対話的なコントロールを作成するために使用します。"><code>&lt;input&gt;</code></a> 要素における入力種類の追加、データバリデーションなどが含まれています。</dd>
 <dt><a href="/ja/docs/Sections_and_outlines_of_an_HTML5_document">HTML5 Sections</a></dt>
 <dd>Gecko は文書におけるセクションに関する新しい HTML5 要素をサポートします。: <a href="/ja/docs/Web/HTML/Element/article" title="HTML の &lt;article> 要素は文書、ページ、アプリケーション、サイトなどの中で自己完結しており、 (集合したものの中で) 個別に配信や再利用を行うことを意図した構成物を表します。"><code>&lt;article&gt;</code></a>、<a href="/ja/docs/Web/HTML/Element/section" title="HTML の &lt;section> 要素は、 HTML 文書の中で単独のセクション (区間) を表します。セクションを表現するより意味的に具体的な要素がない場合に使用します。"><code>&lt;section&gt;</code></a>、<a href="/ja/docs/Web/HTML/Element/nav" title="HTML の &lt;nav> 要素は、現在の文書内の他の部分や他の文書へのナビゲーションリンクを提供するためのセクションを表します。ナビゲーションセクションの一般的な例としてメニュー、目次、索引などがあります。"><code>&lt;nav&gt;</code></a>、<a href="/ja/docs/Web/HTML/Element/aside" title="HTML の &lt;aside> 要素は、文書のメインコンテンツと間接的な関係しか持っていない文書の部分を表現します。"><code>&lt;aside&gt;</code></a>、 <a href="/ja/docs/Web/HTML/Element/hgroup" title="HTML の &lt;hgroup> 要素は、文書のセクションの、複数レベルの見出しを表します。これは &lt;h1>–&lt;h6> 要素のセットをグループ化します。"><code>&lt;hgroup&gt;</code></a>、<a href="/ja/docs/Web/HTML/Element/header" title="HTML の &lt;header> 要素は、導入的なコンテンツ、ふつうは導入部やナビゲーション等のグループを表します。見出し要素だけでなく、ロゴ、検索フォーム、作者名、その他の要素を含むこともできます。"><code>&lt;header&gt;</code></a> および <a href="/ja/docs/Web/HTML/Element/footer" title="HTML の &lt;footer> 要素 は、直近の区分コンテンツまたは区分化ルート要素のフッターを表します。フッターには通常、そのセクションの著作者に関する情報、関連文書へのリンク、著作権情報等を含めます。"><code>&lt;footer&gt;</code></a>。</dd>
 <dt><a href="/ja/docs/HTML/Global_attributes#attr-hidden">HTML5 の hidden 属性</a></dt>
 <dd>この属性は、すべての要素に共通であり、Web ページでユーザに現在は関係しないコンテントを隠すために用いられます。</dd>
 <dt>その他の HTML5 要素</dt>
 <dd>Gecko は次の新しい HTML5 要素もサポートします。: <a href="/ja/docs/Web/HTML/Element/mark" title="HTML の文字列マーク要素 (&lt;mark>) は、周囲の文脈の中でマークを付けた部分の関連性や重要性のために、参照や記述の目的で目立たせたり強調したりする文字列を表します。"><code>&lt;mark&gt;</code></a>、<a href="/ja/docs/Web/HTML/Element/figure" title="HTML の &lt;figure> (任意のキャプション付きの図) 要素は、図表などの自己完結型のコンテンツを表し、任意で (&lt;figcaption>) 要素を使用して表されるキャプションを伴います。"><code>&lt;figure&gt;</code></a> および <a href="/ja/docs/Web/HTML/Element/figcaption" title="HTML の &lt;figcaption> 要素または図キャプション要素は、親の &lt;figure> 要素内にあるその他のコンテンツを説明するキャプションや凡例を表します。"><code>&lt;figcaption&gt;</code></a>。</dd>
 <dt><a href="/ja/docs/WebSockets">WebSocket</a></dt>
 <dd>Web アプリケーションとサーバーの間でリアルタイムコミュニケーションを行うための WebSocket API を利用するためのガイド。</dd>
</dl>

<h4 id="Canvas_improvements" name="Canvas_improvements">Canvas improvements</h4>

<p>The following changes were made to the <a href="/ja/docs/Web/API/CanvasRenderingContext2D" title="Canvas API の CanvasRenderingContext2D インターフェイスは、&lt;canvas> 要素に描画するための 2D レンダリングコンテキストを提供します。図形、文字、画像、その他のオブジェクトを描画するのに使用します。"><code>CanvasRenderingContext2D</code></a> interface to bring our <a href="/ja/docs/Web/HTML/Element/canvas" title="HTML の &lt;canvas> 要素 と Canvas スクリプティング API や WebGL API を使用して、グラフィックやアニメーションを描画することができます。"><code>&lt;canvas&gt;</code></a> implementation closer to being in line with the specification:</p>

<ul>
 <li>Specifying a negative radius when calling <code>arc()</code> now correctly throws an <code>INDEX_SIZE_ERR</code> exception.</li>
 <li>Specifying non-finite values when calling <code>createLinearGradient()</code> and <code>createRadialGradient()</code> now throws <code>NOT_SUPPORTED_ERR</code> instead of <code>SYNTAX_ERR</code>.</li>
 <li>Setting <code>miterLimit</code> to a negative value no longer throws an exception; instead, it properly ignores non-positive values.</li>
 <li>Setting <code>lineWidth</code> to a negative value no longer throws an exception; instead, it properly ignores non-positive values.</li>
 <li>The <code>putImageData()</code> method now supports the optional parameters <code>dirtyX</code>, <code>dirtyY</code>, <code>dirtyWidth</code>, and <code>dirtyHeight</code>.</li>
</ul>

<h4 id="Miscellaneous_HTML_changes" name="Miscellaneous_HTML_changes">小さな HTML の変更</h4>

<ul>
 <li><a href="/ja/docs/Web/HTML/Element/textarea" title="HTML の &lt;textarea> 要素は、複数行のプレーンテキスト編集コントロールを表し、レビューのコメントやお問い合わせフォーム等のように、ユーザーが大量の自由記述テキストを入力できるようにするときに便利です。"><code>&lt;textarea&gt;</code></a> 要素をデフォルトでサイズ変更できるようになりました。これを無効にするために <a href="/ja/docs/Web/CSS/resize" title="CSS の resize プロパティは、要素の寸法を変更できるかどうか、もしそうなら、どの方向に変更できるかを設定します。"><code>resize</code></a> CSS プロパティが利用できます。</li>
 <li><code>canvas.getContext</code> および <code>canvas.toDataURL</code> が認識できない引数を指定して呼び出したときに例外を投げなくなりました。</li>
 <li><a href="/ja/docs/Web/HTML/Element/canvas" title="HTML の &lt;canvas> 要素 と Canvas スクリプティング API や WebGL API を使用して、グラフィックやアニメーションを描画することができます。"><code>&lt;canvas&gt;</code></a> 要素に Mozilla 固有の <code>mozGetAsFile()</code> メソッドが追加されました。これを用いることで、Canvas の内容である画像を含んだメモリベースのファイルを保持できます。詳細は <a href="/ja/docs/Web/API/HTMLCanvasElement" title="HTMLCanvasElementインタフェースはcanvas要素のレイアウトや表現の操作のための属性やメソッドを提供します。HTMLCanvasElementはHTMLElementインタフェースのプロパティやメソッドも利用可能です。"><code>HTMLCanvasElement</code></a> を参照してください。</li>
 <li><code>canvas2dcontext.lineCap</code> および <code>canvas2dcontext.lineJoin</code> が認識できない値を設定したときに例外を投げなくなりました。</li>
 <li><code>canvas2dcontext.globalCompositeOperation</code> が認識できない値を設定したときに例外を投げなくなりました。また、非標準の値 <code>darker</code> をサポートしなくなりました。</li>
 <li>他のブラウザでは実装されておらず、非推奨 な要素である <a href="/ja/docs/Web/HTML/Element/spacer" title="&lt;spacer> は、ウェブページにホワイトスペースを挿入するための廃止された HTML 要素です。ウェブデザイナーによって用いられていた 1px の透過 GIF 画像 (いわゆるスペーサー GIF) の挿入と同様の効果を実現するために Netscape 社が実装したものです。しかし &lt;spacer> はほとんどの主要ブラウザーで対応されず、また、同様の効果は CSS を用いて実現可能です。"><code>&lt;spacer&gt;</code></a> 要素のサポートが無くなりました。</li>
 <li>The <a href="/ja/docs/Web/HTML/Element/isindex" title="&lt;isindex> は廃止された HTML 要素であり、文書に問い合わせを行うためのテキストフィールドをページに追加します。"><code>&lt;isindex&gt;</code></a> 要素が、<a href="/ja/docs/Web/API/Document/createElement" title="HTML ドキュメントにおいて Document.createElement() メソッドは、tagName で指定した HTML 要素を生成する、あるいは tagName を認識できない場合に HTMLUnknownElement を生成します。XUL ドキュメントでは、指定した XUL 要素を生成します。その他のドキュメントでは、null 名前空間 URI の要素を生成します。"><code>document.createElement()</code></a> メソッドによって作成されたときに、 一切プロパティもメソッドも持たない単純な要素として作成されるようになりました。</li>
 <li>Gecko に <a href="/ja/docs/Web/HTML/Element/input" title="HTML の &lt;input> 要素は、ユーザーからデータを受け取るための、ウェブベースのフォーム用の対話的なコントロールを作成するために使用します。"><code>&lt;input&gt;</code></a> 要素での <code>click() </code>メソッドの呼び出しが追加されました。このメソッドを用いることでファイル選択ダイアログが開けます。<a href="/ja/docs/Using_files_from_web_applications">Web アプリケーションからファイルを利用する</a> の記事内の <a href="/ja/docs/Using_files_from_web_applications#Using_hidden_file_input_elements_using_the_click%28%29_method">例</a> を参照してください。</li>
 <li><a href="/ja/docs/Web/HTML/Element/input" title="HTML の &lt;input> 要素は、ユーザーからデータを受け取るための、ウェブベースのフォーム用の対話的なコントロールを作成するために使用します。"><code>&lt;input&gt;</code></a> 要素に新しい <a href="/ja/docs/HTML/Element/Input#attr-mozactionhint"><code>mozactionhint</code></a> 属性が追加されました。これを用いることで仮想キーボード上でのエンターキーのラベルを指定できます。</li>
 <li><a href="/ja/docs/Web/HTML/Element/iframe" title="HTML のインラインフレーム要素 (&lt;iframe>) は、入れ子になった閲覧コンテキストを表現し、現在の HTML ページに他のページを埋め込むことができます。"><code>&lt;iframe&gt;</code></a>、<a href="/ja/docs/Web/HTML/Element/noembed" title="&lt;noembed> 要素は廃止された、標準外の方法であり、&lt;embed> 要素に対応していないブラウザーや、ユーザーが仕様とした種類の埋め込みコンテンツに対応していないブラウザーで代替または「フォールバック」コンテンツを提供するものです。"><code>&lt;noembed&gt;</code></a>、および <a href="/ja/docs/Web/HTML/Element/noframes" title="&lt;noframes> は、古い HTML における No Frames または frame fallback 要素であり、 &lt;frame> 要素に対応していない（または対応を無効化した）ブラウザーのためのコンテンツを提供します。"><code>&lt;noframes&gt;</code></a> 要素内の <a href="/ja/docs/Web/HTML/Element/script" title="HTML の &lt;script> 要素は、実行できるコードを埋め込んだり参照したりするために使用されます。ふつうは JavaScript のコードの埋め込みや参照に使用されます。"><code>&lt;script&gt;</code></a> 要素が実行されるようになりました。以前のバージョンの Firefox ではこれらの要素内での実行はされませんでした。これは仕様準拠であり、他のブラウザの挙動と合致します。</li>
</ul>

<h3 id="CSS" name="CSS">CSS</h3>

<dl>
 <dt><a href="/ja/docs/CSS/CSS_transitions">CSS transitions</a></dt>
 <dd>新しい CSS transitions サポートが Firefox 4 では利用できるようになりました。</dd>
 <dt>CSS での算出値</dt>
 <dd><a href="/ja/docs/Web/CSS/-moz-calc" title="この項目についての文書はまだ書かれていません。書いてみませんか？"><code>-moz-calc</code></a> のサポートが追加されました。これを用いることで、<a href="/ja/docs/Web/CSS/length" title="CSS の &lt;length> データ型は、長さの値を表します。長さは width, height, margin, padding, border-width, font-size, text-shadow など数多くの CSS プロパティで使用されています。"><code>&lt;length&gt;</code></a> の値を数式で指定できます。</dd>
 <dt>セレクタのグルーピング</dt>
 <dd>セレクタをグループ化しコンビネータを分解する <a href="/ja/docs/Web/CSS/:-moz-any" title="この項目についての文書はまだ書かれていません。書いてみませんか？"><code>:-moz-any</code></a> がサポートされました。</dd>
 <dt>背景画像の部分領域のサポート</dt>
 <dd><a href="/ja/docs/Web/CSS/-moz-image-rect" title="この項目についての文書はまだ書かれていません。書いてみませんか？"><code>-moz-image-rect</code></a> 関数を用いることで、画像の一部分の領域 (subrectangle)を背景画像として利用できるようになります。</dd>
 <dt>CSS touch プロパティ群</dt>
 <dd>touch プロパティ群が追加されました。詳細と正式な記事名は後日追記予定です。</dd>
 <dt><a href="/ja/docs/CSS/-moz-element">CSS 背景として任意の要素を使用する</a></dt>
 <dd><a href="/ja/docs/Web/CSS/-moz-element" title="この項目についての文書はまだ書かれていません。書いてみませんか？"><code>-moz-element</code></a> CSS 関数と <a href="/ja/docs/Web/API/Document/mozSetImageElement" title="この項目についての文書はまだ書かれていません。書いてみませんか？"><code>document.mozSetImageElement()</code></a> DOM 関数を用いることで、任意の HTML 要素を背景として使用することができます。</dd>
 <dt><a href="/ja/docs/CSS/Privacy_and_the_:visited_selector">プライバシーと :visited セレクタ</a></dt>
 <dd>CSS セレクタを用いた訪問済みリンクのスタイルについて取得できる情報が変更されました。これはいくつかの Web アプリケーションに影響するかもしれません。</dd>
</dl>

<h4 id="New_CSS_properties" name="New_CSS_properties">新しい CSS プロパティ</h4>

<table class="standard-table">
 <tbody>
  <tr>
   <td class="header">プロパティ</td>
   <td class="header">説明</td>
  </tr>
  <tr>
   <td><a href="/ja/docs/Web/CSS/-moz-font-feature-settings" title="この項目についての文書はまだ書かれていません。書いてみませんか？"><code>-moz-font-feature-settings</code></a></td>
   <td>OpenType フォントの高度な機能を変更できます。</td>
  </tr>
  <tr>
   <td><a href="/ja/docs/Web/CSS/-moz-tab-size" title="この項目についての文書はまだ書かれていません。書いてみませんか？"><code>-moz-tab-size</code></a></td>
   <td>テキストを描画するときのタブ文字 (U+0009) の幅を空白文字数で指定します。</td>
  </tr>
  <tr>
   <td><a href="/ja/docs/Web/CSS/resize" title="CSS の resize プロパティは、要素の寸法を変更できるかどうか、もしそうなら、どの方向に変更できるかを設定します。"><code>resize</code></a></td>
   <td>サイズ変更可能な要素の方向を制御できます。</td>
  </tr>
 </tbody>
</table>

<h4 id="New_CSS_pseudo-classes" name="New_CSS_pseudo-classes">新しい CSS 擬似クラス</h4>

<table class="standard-table">
 <tbody>
  <tr>
   <td class="header">擬似クラス</td>
   <td class="header">説明</td>
  </tr>
  <tr>
   <td><a href="/ja/docs/Web/CSS/:-moz-handler-crashed" title="この項目についての文書はまだ書かれていません。書いてみませんか？"><code>:-moz-handler-crashed</code></a></td>
   <td>プラグインがクラッシュした要素の表示に用いられます。</td>
  </tr>
  <tr>
   <td><a href="/ja/docs/Web/CSS/:-moz-placeholder" title=":-moz-placeholder はプレースホルダを表示するフォーム要素にマッチします。この擬似クラスにより、Web 開発者やテーマデザイナーがプレースホルダの表示 (デフォルトは薄い灰色) をカスタマイズすることができます。"><code>:-moz-placeholder</code></a></td>
   <td>フォームフィールドのガイドテキストに適用されます。</td>
  </tr>
  <tr>
   <td><a href="/ja/docs/Web/CSS/:-moz-submit-invalid" title="この項目についての文書はまだ書かれていません。書いてみませんか？"><code>:-moz-submit-invalid</code></a></td>
   <td>1 つ、もしくは、複数のフォームフィールドの入力が妥当でないときのフォームの送信ボタンに適用されます。</td>
  </tr>
  <tr>
   <td><a href="/ja/docs/Web/CSS/:-moz-window-inactive" title="この項目についての文書はまだ書かれていません。書いてみませんか？"><code>:-moz-window-inactive</code></a></td>
   <td>アクティブでないウィンドウの要素に適用されます。</td>
  </tr>
  <tr>
   <td><a href="/ja/docs/Web/CSS/:invalid" title="CSS の :invalid 疑似クラスは、内容の検証に失敗した &lt;input> 要素 や &lt;form> 要素を表します。"><code>:invalid</code></a></td>
   <td>入力が妥当でない <a href="/ja/docs/Web/HTML/Element/input" title="HTML の &lt;input> 要素は、ユーザーからデータを受け取るための、ウェブベースのフォーム用の対話的なコントロールを作成するために使用します。"><code>&lt;input&gt;</code></a> フィールドに自動的に適用されます。</td>
  </tr>
  <tr>
   <td><a href="/ja/docs/Web/CSS/:optional" title="CSS の :optional 疑似クラスは、 required 属性が設定されていない &lt;input>, &lt;select>, &lt;textarea> 要素を表します。"><code>:optional</code></a></td>
   <td><code>required</code> 属性を指定していない <a href="/ja/docs/Web/HTML/Element/input" title="HTML の &lt;input> 要素は、ユーザーからデータを受け取るための、ウェブベースのフォーム用の対話的なコントロールを作成するために使用します。"><code>&lt;input&gt;</code></a> フィールドに自動的に適用されます。</td>
  </tr>
  <tr>
   <td><a href="/ja/docs/Web/CSS/:required" title="CSS の :required 疑似クラスは、 required 属性が設定されている &lt;input>, &lt;select>, &lt;textarea> 要素を表します。"><code>:required</code></a></td>
   <td><code>required</code> 属性を指定している <a href="/ja/docs/Web/HTML/Element/input" title="HTML の &lt;input> 要素は、ユーザーからデータを受け取るための、ウェブベースのフォーム用の対話的なコントロールを作成するために使用します。"><code>&lt;input&gt;</code></a> フィールドに自動的に適用されます。</td>
  </tr>
  <tr>
   <td><a href="/ja/docs/Web/CSS/:valid" title="CSS の :invalid 疑似クラスは、内容の検証に成功した &lt;input> 要素 やその他の &lt;form> 要素を表します。これにより、有効な入力欄に、データの形式が適切であることをユーザーが確認しやすくなる外観を簡単に適用できるようになります。"><code>:valid</code></a></td>
   <td>入力が妥当であると判断された <a href="/ja/docs/Web/HTML/Element/input" title="HTML の &lt;input> 要素は、ユーザーからデータを受け取るための、ウェブベースのフォーム用の対話的なコントロールを作成するために使用します。"><code>&lt;input&gt;</code></a> フィールドに自動的に適用されます。</td>
  </tr>
 </tbody>
</table>

<h4 id="New_CSS_pseudo-selectors" name="New_CSS_pseudo-selectors">新しい CSS 擬似セレクタ</h4>

<table class="standard-table">
 <tbody>
  <tr>
   <td class="header">擬似セレクタ</td>
   <td class="header">説明</td>
  </tr>
  <tr>
   <td><a href="/ja/docs/Web/CSS/:-moz-focusring" title="CSS の :-moz-focusring 疑似クラスは、 :focus 疑似クラスに似た Mozilla 拡張ですが、現在フォーカスが当たっていて、かつフォーカスリングやその他のインジケーターがその周りに描かれる場合のみ一致します。"><code>:-moz-focusring</code></a></td>
   <td>Gecko がフォーカスインジケータを描画すべきとしている要素の見え方を指定できます。</td>
  </tr>
 </tbody>
</table>

<h4 id="New_CSS_functions" name="New_CSS_functions">新しい CSS 関数</h4>

<table class="standard-table">
 <tbody>
  <tr>
   <td class="header">関数</td>
   <td class="header">説明</td>
  </tr>
  <tr>
   <td><a href="/ja/docs/Web/CSS/:-moz-any" title="この項目についての文書はまだ書かれていません。書いてみませんか？"><code>:-moz-any</code></a></td>
   <td>セレクタをグループ化しコンビネータを分解できます。</td>
  </tr>
  <tr>
   <td><a href="/ja/docs/Web/CSS/-moz-calc" title="この項目についての文書はまだ書かれていません。書いてみませんか？"><code>-moz-calc</code></a></td>
   <td><code><span style="font-family: verdana,tahoma,sans-serif;"><a href="/ja/docs/Web/CSS/length" title="CSS の &lt;length> データ型は、長さの値を表します。長さは width, height, margin, padding, border-width, font-size, text-shadow など数多くの CSS プロパティで使用されています。"><code>&lt;length&gt;</code></a> の値を数式で指定できます。</span></code></td>
  </tr>
  <tr>
   <td><a href="/ja/docs/Web/CSS/-moz-element" title="この項目についての文書はまだ書かれていません。書いてみませんか？"><code>-moz-element</code></a></td>
   <td>任意の要素を <a href="/ja/docs/Web/CSS/background-image" title="CSS の background-image プロパティは、要素に1つ以上の背景画像を設定します。"><code>background-image</code></a> および <a href="/ja/docs/Web/CSS/background" title="CSS の background 一括指定プロパティは、色、画像、原点と寸法、反復方法など、背景に関するすべてのスタイルプロパティを一括で設定します。"><code>background</code></a> の背景として使用できます。</td>
  </tr>
  <tr>
   <td><a href="/ja/docs/Web/CSS/-moz-image-rect" title="この項目についての文書はまだ書かれていません。書いてみませんか？"><code>-moz-image-rect</code></a></td>
   <td>画像の一部分を <a href="/ja/docs/Web/CSS/background-image" title="CSS の background-image プロパティは、要素に1つ以上の背景画像を設定します。"><code>background-image</code></a> もしくは <a href="/ja/docs/Web/CSS/background" title="CSS の background 一括指定プロパティは、色、画像、原点と寸法、反復方法など、背景に関するすべてのスタイルプロパティを一括で設定します。"><code>background</code></a>で利用できます。</td>
  </tr>
 </tbody>
</table>

<h4 id="Renamed_CSS_properties" name="Renamed_CSS_properties">改名された CSS プロパティ</h4>

<table class="standard-table">
 <thead>
  <tr>
   <td class="header">旧名称</td>
   <td class="header">新名称</td>
   <td class="header">備考</td>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td><code>-moz-background-size</code></td>
   <td><a href="/ja/docs/Web/CSS/background-size" title="CSS の background-size プロパティは、要素の背景画像の寸法を設定します。画像は自然な寸法になったり、引き伸ばされたり、利用可能な領域に収まるように縮小されたりします。"><code>background-size</code></a></td>
   <td><code>-moz-background-size</code> という名称はサポートされません。</td>
  </tr>
  <tr>
   <td><code>-moz-border-radius</code></td>
   <td><a href="/ja/docs/Web/CSS/border-radius" title="CSS の border-radius プロパティは、要素の境界の外側の角を丸めます。1つの半径を設定すると円の角になり、2つの半径を設定すると楕円の角になります。"><code>border-radius</code></a></td>
   <td>旧名称は、サイトを更新するための時間を考慮して、限られた期間サポートされます。描画の変更も仕様の最新版に適合するようになります。</td>
  </tr>
  <tr>
   <td><code>-moz-box-shadow</code></td>
   <td><a href="/ja/docs/Web/CSS/box-shadow" title="CSS の box-shadow プロパティは、要素のフレームの周囲にシャドウ効果を追加します。コンマで区切ることで、複数の効果を指定することができます。"><code>box-shadow</code></a></td>
   <td></td>
  </tr>
 </tbody>
</table>

<h4 id="Miscellaneous_CSS_changes" name="Miscellaneous_CSS_changes">小さな CSS の変更</h4>

<ul>
 <li><a href="/ja/docs/Web/CSS/text-shadow" title="CSS の text-shadow プロパティはテキストに影を追加します。文字列及びその装飾に適用される影のコンマで区切られたリストを受け付けます。"><code>text-shadow</code></a> プロパティのぼかし範囲が 300 までに制限されるようになりました。これは健全さとパフォーマンスの理由によるものです。</li>
 <li><a href="/ja/docs/Web/CSS/overflow" title="CSS の overflow プロパティは、要素の内容が多すぎてブロック整形コンテキストに収まらない場合にどうするかを設定します。これは overflow-x および overflow-y の一括指定です。"><code>overflow</code></a> プロパティがテーブルグループ要素 (<code>&lt;thead&gt;</code>、<code>&lt;tbody&gt;</code>、および <code>&lt;tfoot&gt;</code>) に適用されなくなりました。</li>
 <li><a href="/ja/docs/Web/CSS/-moz-appearance" title="この項目についての文書はまだ書かれていません。書いてみませんか？"><code>-moz-appearance</code></a> プロパティが要素に境界のない Aero Glass の見た目を適用する <code>-moz-win-borderless-glass 値をサポートするようになりました。</code></li>
 <li><code><a href="/ja/docs/CSS/Media_queries#-moz-device-pixel-ratio">-moz-device-pixel-ratio</a></code> メディア機能が追加されました。これを用いることで、<a href="/ja/docs/CSS/Media_queries">Media Query</a> で用いられる、CSS ピクセルを基準としたデバイスのピクセル比率を指定できます。</li>
 <li>Gecko の <a href="/ja/docs/CSS-2_Quick_Reference/Units">CSS 単位の</a> 扱いが他のブラウザにより良く適合するように、また、絶対的長さをデバイスの DPI を基準にした画面ピクセル数により的確に変換するように修正されました。</li>
</ul>

<h3 id="Graphics_and_video" name="Graphics_and_video">グラフィックとビデオ</h3>

<dl>
 <dt><a href="/ja/docs/WebGL">WebGL</a></dt>
 <dd>開発中の WebGL 標準が Firefox でサポートされました。</dd>
 <dt><a href="/ja/docs/Optimizing_graphics_performance">グラフィックパフォーマンスの最適化</a></dt>
 <dd>Firefox 4 でグラフィックとビデオのパフォーマンスを最大限引き出すための Tips &amp; Tricks。</dd>
 <dt><a href="/ja/docs/Media_formats_supported_by_the_audio_and_video_elements#WebM">WebM ビデオのサポート</a></dt>
 <dd>新しいオープンな <a href="http://www.webmproject.org/">WebM</a> ビデオフォーマットが Gecko2.0 でサポートされます。このサポートは 6 月 9 日以降のナイトリーに含まれています。</dd>
 <dt><a href="/ja/docs/SVG/SVG_animation_with_SMIL">SMIL による SVG アニメーション</a></dt>
 <dd>SVG の SMIL アニメーションのサポートが利用できるようになりました。<a href="https://bugzilla.mozilla.org/show_bug.cgi?id=482402" title='FIXED: Enable "svg.smil.enabled" pref by default'>バグ 482402</a> を参照してください。</dd>
 <dt>画像と CSS 背景としての SVG の利用</dt>
 <dd>SVG を <a href="/ja/docs/Web/HTML/Element/img" title="HTML の &lt;img> 要素は、文書に画像を埋め込みます。"><code>&lt;img&gt;</code></a> 要素とともに、また、CSS の <a href="/ja/docs/Web/CSS/background-image" title="CSS の background-image プロパティは、要素に1つ以上の背景画像を設定します。"><code>background-image</code></a> で利用することができるようになりました。</dd>
 <dt>メディア要素での <code>buffered</code> 属性サポート</dt>
 <dd><a href="/ja/docs/Web/HTML/Element/video" title="HTML の映像要素 (&lt;video>) は、文書中に映像再生に対応するメディアプレイヤーを埋め込みます。"><code>&lt;video&gt;</code></a> および <a href="/ja/docs/Web/HTML/Element/audio" title="この項目についての文書はまだ書かれていません。書いてみませんか？"><code>&lt;audio&gt;</code></a> 要素での <code>buffered</code> 属性がサポートされました。これを用いることでメディアファイルでバッファリングされた範囲が判断可能になります。これをサポートするために <a href="/ja/docs/Web/API/TimeRanges" title="この項目についての文書はまだ書かれていません。書いてみませんか？"><code>TimeRanges</code></a> DOM インタフェースが実装されました。</dd>
 <dt>メディア要素での <code>preload</code> 属性</dt>
 <dd>HTML5 仕様から <code>preload</code> 属性が実装されました。これは以前実装された（そしてもうサポートされない）<code>autobuffer</code> 属性を置き換えものです。これは <a href="/ja/docs/Web/HTML/Element/video" title="HTML の映像要素 (&lt;video>) は、文書中に映像再生に対応するメディアプレイヤーを埋め込みます。"><code>&lt;video&gt;</code></a> および <a href="/ja/docs/Web/HTML/Element/audio" title="この項目についての文書はまだ書かれていません。書いてみませんか？"><code>&lt;audio&gt;</code></a> 要素、同様に<code><a href="/ja/docs/Mozilla/Tech/XPCOM/Reference/Interface/nsIDOMHTMLMediaElement" title="">nsIDOMHTMLMediaElement</a></code> インタフェースを実装した要素で利用できます。</dd>
 <dt>SVG text 位置指定の改善</dt>
 <dd>SVG <a href="/ja/docs/Web/SVG/Element/text" title="SVG &lt;text> 要素は、テキストからなるグラフィクス要素を定義します。&lt;text> には、他の SVG グラフィクス要素と同じように、グラデーション、パターン、クリッピングパス、マスク、またはフィルターを適用することができます。"><code>&lt;text&gt;</code></a> and <a href="/ja/docs/Web/SVG/Element/tspan" title="&lt;text> 要素の中に &lt;tspan> 要素を組み込むことで、テキストとフォントのプロパティ及び現在のテキストの位置を絶対値または相対値を用いた座標で調節することができます。"><code>&lt;tspan&gt;</code></a> 要素で <code>x</code>、<code>y</code>、<code>dx</code>、および <code>dy</code> プロパティの値のためのリストを指定できるようになりました。これを用いることで、文字列中の各文字の位置を個別に制御できます。</dd>
</dl>

<h3 id="DOM" name="DOM">DOM</h3>

<dl>
 <dt><a href="/ja/docs/JavaScript_typed_arrays">JavaScript 型付き配列</a></dt>
 <dd>JavaScript 型付き配列 (typed arrays) のサポートが追加されました。これを用いることで、ネイティブデータ型を用いた生のデータを含むバッファを扱えます。 <a href="/ja/docs/DOM/File">File API</a>、<a href="/ja/docs/WebGL">WebGL</a>、および <a href="/ja/docs/WebSockets">WebSockets</a> を含む、いくつかの API でこれを用いることができます。</dd>
 <dt>範囲の境界領域の保持</dt>
 <dd><a href="/ja/docs/Web/API/Range" title="Range インターフェイスとは document の断片で、ある document 中のノードやテキストノードの一部を含むことのできるものです。"><code>Range</code></a> オブジェクトに <a href="/ja/docs/Web/API/Range/getClientRects" title="この項目についての文書はまだ書かれていません。書いてみませんか？"><code>range.getClientRects()</code></a> および <a href="/ja/docs/Web/API/Range/getBoundingClientRect" title="この項目についての文書はまだ書かれていません。書いてみませんか？"><code>range.getBoundingClientRect()</code></a> メソッドが追加されました。</dd>
 <dt>任意の要素上でのマウスイベントのキャプチャ</dt>
 <dd>Internet Explorer 由来の <code>setCapture()</code> と <code>releaseCapture() </code>API のサポートが追加されました。<a href="https://bugzilla.mozilla.org/show_bug.cgi?id=503943" title="FIXED: Need a way to grab mouse events on arbitrary elements (implement setCapture/releaseCapture)">バグ 503943</a> を参照してください。</dd>
 <dt><a href="/ja/docs/DOM/Manipulating_the_browser_history">ブラウザ履歴の操作</a></dt>
 <dd><a href="/ja/docs/Web/API/Window/history" title="The Window.history read-only property returns a reference to the History object, which provides an interface for manipulating the browser session history (pages visited in the tab or frame that the current page is loaded in)."><code>window.history</code></a> オブジェクトを通して利用できる、既存のドキュメント履歴オブジェクトが新しい HTML5 の <code>pushState()</code> と <code>replaceState()</code> メソッドをサポートするようになりました。</dd>
 <dt><a href="/ja/docs/DOM/Animations_using_MozBeforePaint">MozBeforePaint を用いたアニメーション</a></dt>
 <dd>追加された新しいイベントと <a href="/ja/docs/Web/API/Window/mozRequestAnimationFrame" title="この項目についての文書はまだ書かれていません。書いてみませんか？"><code>window.mozRequestAnimationFrame()</code></a> メソッドおよび <a href="/ja/docs/Web/API/Window/mozAnimationStartTime" title="この項目についての文書はまだ書かれていません。書いてみませんか？"><code>window.mozAnimationStartTime</code></a> プロパティを組み合わせることで、互いに同期したアニメーションを作成する方法が提供されます。</dd>
 <dt>タッチイベントとマルチタッチイベント</dt>
 <dd>タッチイベントとマルチタッチイベントのサポートが追加されました。</dd>
</dl>

<h4 id="HTML_elements_DOM_interfaces_have_changed" name="HTML_elements'_DOM_interfaces_have_changed">HTML 要素の DOM インタフェースが変更されました</h4>

<p>いくつかの HTML 要素に関連づけられた DOM インタフェースが、以下のように、 HTML5 仕様で要求されるひとつのインタフェースに変更されました。</p>

<table class="standard-table">
 <tbody>
  <tr>
   <td class="header">Firefox 3.6 でのインタフェース</td>
   <td class="header">Firefox 4 でのインタフェース</td>
   <td class="header">HTML 要素</td>
  </tr>
  <tr>
   <td><a href="/ja/docs/Web/API/HTMLSpanElement" title="HTMLSpanElement インターフェイスは &lt;span> 要素を表し、 HTMLElement から派生していますが、それ以外のプロパティやメソッドを追加していません。"><code>HTMLSpanElement</code></a></td>
   <td><code><a href="/ja/docs/DOM/HTMLElement">HTMLElement</a></code></td>
   <td><a href="/ja/docs/Web/HTML/Element/abbr" title="HTML の略語要素 (&lt;abbr>) は略語や頭字語を表します。任意で title 属性で、略語の完全形または説明を提供することができます。"><code>&lt;abbr&gt;</code></a>, <a href="/ja/docs/Web/HTML/Element/acronym" title="HTML の頭字語要素 (&lt;acronym>) は、頭字語または略語の単語を構成する文字の並びを明示することができます。この要素は HTML5 で削除されました。 &lt;abbr> 要素を使用してください。"><code>&lt;acronym&gt;</code></a>, <a href="/ja/docs/Web/HTML/Element/address" title="HTML の &lt;address> 要素は、これを含んでいる HTML が個人、団体、組織の連絡先を提供していることを示します。"><code>&lt;address&gt;</code></a>, <a href="/ja/docs/Web/HTML/Element/b" title="HTML の注目付け要素 (&lt;b>) は、要素の内容に読み手の注意を惹きたい場合で、他の特別な重要性が与えられないものに使用します。"><code>&lt;b&gt;</code></a>, <a href="/ja/docs/Web/HTML/Element/bdo" title="HTML の双方向文字列上書き要素 (&lt;bdo>) は、現在の文字列の方向を上書きし、中の文字列が異なる方向に描画されるようにします。"><code>&lt;bdo&gt;</code></a>, <a href="/ja/docs/Web/HTML/Element/big" title="廃止された HTML の Big 要素 (&lt;big>) は、内包するテキストを周りの文字列よりも1段階大きいフォントの大きさで描画します（例えば medium が large になります）。"><code>&lt;big&gt;</code></a>, <a href="/ja/docs/Web/HTML/Element/blink" title="HTML の点滅要素 (&lt;blink>) は内包するテキストをゆっくり点滅させるための、標準外の要素です。"><code>&lt;blink&gt;</code></a>, <a href="/ja/docs/Web/HTML/Element/center" title="廃止済みの HTML の中央揃え要素 (&lt;center>) は、中に含まれるブロックレベルまたはインラインコンテンツを中央揃えして表示するブロックレベル要素です。"><code>&lt;center&gt;</code></a>, <a href="/ja/docs/Web/HTML/Element/cite" title="HTML の引用元要素 (&lt;cite>) は、引用された創作物の参照を表し、作品のタイトルを含む必要があります。参照は、引用メタデータに関する利用場面に合わせた慣習に応じて省略形が用いられることがあります。"><code>&lt;cite&gt;</code></a>, <a href="/ja/docs/Web/HTML/Element/code" title="HTML の &lt;code> 要素は、コンピューターコードの短い断片の文字列であると識別できるような外見のコンテンツを表示します。"><code>&lt;code&gt;</code></a>, <a href="/ja/docs/Web/HTML/Element/dd" title="HTML の &lt;dd> 要素は、定義リスト要素 (&lt;dl>) 内で、先行する用語 (&lt;dt>) の説明、定義、値などを示します。"><code>&lt;dd&gt;</code></a>, <a href="/ja/docs/Web/HTML/Element/dfn" title="HTML の定義要素 (&lt;dfn>) は、定義句や文の文脈の中で定義している用語を示すために用いられます。"><code>&lt;dfn&gt;</code></a>, <a href="/ja/docs/Web/HTML/Element/dt" title="HTML の &lt;dt> 要素は、説明又は定義リストの中で用語を表す部分であり、 &lt;dl> の子要素としてのみ用いることができます。"><code>&lt;dt&gt;</code></a>, <a href="/ja/docs/Web/HTML/Element/em" title="HTML の &lt;em> 要素は、強調されたテキストを示します。&lt;em> 要素は入れ子にすることができ、入れ子の段階に応じてより強い程度の強調を表すことができます。"><code>&lt;em&gt;</code></a>, <a href="/ja/docs/Web/HTML/Element/i" title="HTML の &lt;i> 要素は、何らかの理由で他のテキストと区別されるテキストの範囲を表します。例えば、技術用語、外国語のフレーズ、架空の人物の思考などです。英文においてはよく斜体で表示されるものです。"><code>&lt;i&gt;</code></a>, <a href="/ja/docs/Web/HTML/Element/kbd" title="HTML のキーボード入力要素 (&lt;kbd>) はキーボード、音声入力、その他の入力端末からのユーザーによる文字入力を表す行内の文字列の区間を表します。"><code>&lt;kbd&gt;</code></a>, <a href="/ja/docs/Web/HTML/Element/listing" title="HTML の Listing 要素 (&lt;listing>) は、開始タグと終了タグの間にあるテキストを HTML として解釈せず、等幅フォントを使用して表示します。HTML 2 標準では、1 行が 132 文字を超えない場合は改行すべきではないと勧告しています。"><code>&lt;listing&gt;</code></a>, <a href="/ja/docs/Web/HTML/Element/nobr" title="標準外かつ廃止された HTML の &lt;nobr> 要素は、その内包する文字列の自動改行を無効化します。行内におさまらない文字列は、領域からはみ出てレンダリングされるか、スクロールバーを伴って表示されます。"><code>&lt;nobr&gt;</code></a>, <a href="/ja/docs/Web/HTML/Element/plaintext" title="プレーンテキスト要素 (&lt;plaintext>) は、開始タグ以降のすべてを生のテキストとして表示し、それ以降の HTML を無視します。"><code>&lt;plaintext&gt;</code></a>, <a href="/ja/docs/Web/HTML/Element/s" title="HTML の &lt;s> 要素は取り消し線を引いた文字列を表示します。 &lt;s> 要素はすでに適切または正確ではなくなった事柄を表現します。しかし、文書の修正を示す場合、 &lt;s> 要素は適切ではありません。この場合は &lt;del> と &lt;ins> の方が適しているので、こちらを使用してください。"><code>&lt;s&gt;</code></a>, <a href="/ja/docs/Web/HTML/Element/samp" title="HTML のサンプル要素 (&lt;samp>) は、コンピュータープログラムからのサンプル出力を表す行内文字列を含めるために使用されます。"><code>&lt;samp&gt;</code></a>, <a href="/ja/docs/Web/HTML/Element/small" title="HTML の &lt;small> 要素は、表示上のスタイルとは関係なく、著作権表示や法的表記のような、注釈や小さく表示される文を表します。既定では、 small から x-small のように、一段階小さいフォントでテキストが表示されます。"><code>&lt;small&gt;</code></a>, <a href="/ja/docs/Web/HTML/Element/strike" title="HTML の &lt;strike> 要素 (または HTML 取り消し線要素) は、テキストの上に取り消し線 (水平線) を配置します。"><code>&lt;strike&gt;</code></a>, <a href="/ja/docs/Web/HTML/Element/strong" title="HTML の強い重要性要素 (&lt;strong>) は、内容の重要性、重大性、または緊急性が高いテキストを表します。ブラウザーは一般的に太字で描画します。"><code>&lt;strong&gt;</code></a>, <a href="/ja/docs/Web/HTML/Element/sub" title="HTML の 下付き文字要素 (&lt;sub>) は、表記上の理由で下付き文字として表示するべき行内文字列を指定します。"><code>&lt;sub&gt;</code></a>, <a href="/ja/docs/Web/HTML/Element/sup" title="HTML の 上付き文字要素 (&lt;sup>) は、表記上の理由で上付き文字として表示するべき行内文字列を指定します。"><code>&lt;sup&gt;</code></a>, , <a href="/ja/docs/Web/HTML/Element/tt" title="廃止された HTML テレタイプテキスト要素 (&lt;tt>) は、ユーザーエージェントの既定の等幅フォントで表示される行内文字列を生成します。"><code>&lt;tt&gt;</code></a>, <a href="/ja/docs/Web/HTML/Element/u" title="HTML の非言語的注釈要素 (&lt;u>) は、非言語的に注釈があることを示す方法で表示する行内テキストの区間を示します。"><code>&lt;u&gt;</code></a>, <a href="/ja/docs/Web/HTML/Element/var" title="HTML の変数要素 (&lt;var>) は、数式やプログラムコード内の変数の名前を表します。"><code>&lt;var&gt;</code></a>, <a href="/ja/docs/Web/HTML/Element/xmp" title="xmp (Example) 要素 (&lt;xmp>) は、その開始タグから終了タグまでの間の HTML タグを HTML として解釈せず、等幅フォントでレンダリングします。HTML2 はこれが 1 行当たり 80 文字を表示するのに充分な幅でレンダリングするよう推奨しています。"><code>&lt;xmp&gt;</code></a></td>
  </tr>
  <tr>
   <td><code><a href="/ja/docs/DOM/HTMLDivElement">HTMLDivElement</a></code></td>
   <td><code><a href="/ja/docs/DOM/HTMLElement">HTMLElement</a></code></td>
   <td><a href="/ja/docs/Web/HTML/Element/noembed" title="&lt;noembed> 要素は廃止された、標準外の方法であり、&lt;embed> 要素に対応していないブラウザーや、ユーザーが仕様とした種類の埋め込みコンテンツに対応していないブラウザーで代替または「フォールバック」コンテンツを提供するものです。"><code>&lt;noembed&gt;</code></a>, <a href="/ja/docs/Web/HTML/Element/noframes" title="&lt;noframes> は、古い HTML における No Frames または frame fallback 要素であり、 &lt;frame> 要素に対応していない（または対応を無効化した）ブラウザーのためのコンテンツを提供します。"><code>&lt;noframes&gt;</code></a>, <a href="/ja/docs/Web/HTML/Element/noscript" title="HTML の &lt;noscript> 要素は、このページ上のスクリプトの種類に対応していない場合や、スクリプトの実行がブラウザーで無効にされている場合に表示する HTML の部分を定義します。"><code>&lt;noscript&gt;</code></a></td>
  </tr>
  <tr>
   <td><code><a href="/ja/docs/DOM/HTMLWBRElement">HTMLWBRElement</a></code></td>
   <td><code><a href="/ja/docs/DOM/HTMLElement">HTMLElement</a></code></td>
   <td><a href="/ja/docs/Web/HTML/Element/wbr" title="HTML の &lt;wbr> 要素は、改行可能位置 — テキスト内でブラウザーが任意で改行してよい位置を表しますが、この改行規則は必要のない場合は改行を行いません。"><code>&lt;wbr&gt;</code></a></td>
  </tr>
 </tbody>
</table>

<h4 id="Miscellaneous_DOM_changes" name="Miscellaneous_DOM_changes">小さな DOM の変更</h4>

<ul>
 <li><code>wrap</code> DOM 属性を利用することで、<a href="/ja/docs/Web/HTML/Element/textarea" title="HTML の &lt;textarea> 要素は、複数行のプレーンテキスト編集コントロールを表し、レビューのコメントやお問い合わせフォーム等のように、ユーザーが大量の自由記述テキストを入力できるようにするときに便利です。"><code>&lt;textarea&gt;</code></a> <code>要素の折り返しを </code>DOM によってコントロールできるようになりました。<a href="https://bugzilla.mozilla.org/show_bug.cgi?id=41464" title="FIXED: textarea.wrap not exposed through DOM (IE compatability)">バグ 41464</a></li>
 <li><a href="/ja/docs/Web/API/Document/createElement" title="HTML ドキュメントにおいて Document.createElement() メソッドは、tagName で指定した HTML 要素を生成する、あるいは tagName を認識できない場合に HTMLUnknownElement を生成します。XUL ドキュメントでは、指定した XUL 要素を生成します。その他のドキュメントでは、null 名前空間 URI の要素を生成します。"><code>document.createElement()</code></a> を用いて作成されてドキュメントに追加された <a href="/ja/docs/Web/HTML/Element/script" title="HTML の &lt;script> 要素は、実行できるコードを埋め込んだり参照したりするために使用されます。ふつうは JavaScript のコードの埋め込みや参照に使用されます。"><code>&lt;script&gt;</code></a> 要素が、標準で HTML5 仕様に従って動作するようになりました。 <code>src</code> 属性で指定されたスクリプトは（順番を調整することはせずに）実行可能になりしだい実行され、<code>src</code> 属性で指定されていないスクリプトは同期的に実行されます。<code>src</code> 属性を持つ挿入されたスクリプトを挿入された順番で実行するには、<code>それらに .async=false を指定します。</code></li>
 <li>DOM の <a href="/ja/docs/Web/API/File" title="File インターフェイスは、ファイルについての情報を提供したり、ウェブページ内の JavaScript でその内容にアクセスできるようにしたりします。"><code>file</code></a> オブジェクトが url プロパティを提供するようになりました。</li>
 <li>DOM の <a href="/ja/docs/Web/API/File" title="File インターフェイスは、ファイルについての情報を提供したり、ウェブページ内の JavaScript でその内容にアクセスできるようにしたりします。"><code>file</code></a> オブジェクトに<code>新しく click()</code> メソッドが追加されました。</li>
 <li>XMLHttpRequest で <a href="/ja/docs/XMLHttpRequest/Using_XMLHttpRequest#Using_FormData_objects">FormData</a> がサポートされました。</li>
 <li><a href="/ja/docs/Web/API/Element/isContentEditable" title="この項目についての文書はまだ書かれていません。書いてみませんか？"><code>element.isContentEditable</code></a> プロパティが実装されました。</li>
 <li><a href="/ja/docs/Web/API/Document/currentScript" title="Document.currentScript プロパティは、現在処理中のスクリプトの &lt;script> 要素を返します。"><code>document.currentScript</code></a> プロパティを用いることで、現在実行されている <a href="/ja/docs/Web/HTML/Element/script" title="HTML の &lt;script> 要素は、実行できるコードを埋め込んだり参照したりするために使用されます。ふつうは JavaScript のコードの埋め込みや参照に使用されます。"><code>&lt;script&gt;</code></a> 要素のスクリプトを判別できます。新しく追加された <a href="/ja/docs/Web/API/Element/onbeforescriptexecute" title="この項目についての文書はまだ書かれていません。書いてみませんか？"><code>element.onbeforescriptexecute</code></a> および <a href="/ja/docs/Web/API/Element/onafterscriptexecute" title="この項目についての文書はまだ書かれていません。書いてみませんか？"><code>element.onafterscriptexecute</code></a> イベントは script 要素の実行前後に発生します。</li>
 <li><a href="/ja/docs/DragDrop/DataTransfer"><code>DragTransfer</code></a> オブジェクトに <a href="/ja/docs/DragDrop/DataTransfer#mozSourceNode"><code>mozSourceNode</code></a> プロパティが追加されました。</li>
 <li><a href="/ja/docs/Web/API/Selection" title="このオブジェクトのクラスは window.getSelection() やその他のメソッドによって返されるものです。"><code>Selection</code></a> オブジェクトに <a href="/ja/docs/DOM/Selection/modify"><code>selection.modify()</code></a> メソッドが追加されました。このメソッドを用いると、ブラウザウィンドウでの現在のテキスト選択範囲あるいはカーソル位置を簡単に変更できます。</li>
 <li><code>window.directories</code> オブジェクトと <a href="/ja/docs/Web/API/Window/open" title="指定された名前のブラウザコンテキスト(ウィンドウや &lt;iframe>、タブ)に、指定されたリソースをロードします。該当の名前のコンテキストがない場合、新しいウィンドウを開いてそこにリソースをロードします。"><code>window.open</code></a> の <code>directories</code> 特性（これらは他のブラウザではサポートされていません）が 削除されました。代わりに <code>personalbar</code> を利用してください。<a href="https://bugzilla.mozilla.org/show_bug.cgi?id=474058" title="FIXED: Drop support for window.directories">バグ 474058</a></li>
 <li><a href="/ja/docs/Web/API/Event/mozInputSource" title="この項目についての文書はまだ書かれていません。書いてみませんか？"><code>event.mozInputSource</code></a> プロパティが DOM ユーザインタフェースイベントに追加されました。この非標準プロパティを用いると、イベントを生成したデバイスのタイプを判別できます。</li>
 <li><a href="/ja/docs/Web/API/Document/onreadystatechange" title="この項目についての文書はまだ書かれていません。書いてみませんか？"><code>document.onreadystatechange</code></a> イベントが実装されました。</li>
 <li><a href="/ja/docs/Web/API/Document/createElement" title="HTML ドキュメントにおいて Document.createElement() メソッドは、tagName で指定した HTML 要素を生成する、あるいは tagName を認識できない場合に HTMLUnknownElement を生成します。XUL ドキュメントでは、指定した XUL 要素を生成します。その他のドキュメントでは、null 名前空間 URI の要素を生成します。"><code>document.createElement</code></a> メソッドが Quirks モードでタグ名の前後の <code>&lt;</code> と <code>&gt;</code> を受け入れないようになりました。</li>
 <li><a href="/ja/docs/Web/API/Element/setCapture" title="mousedownイベントの処理中にこのメソッドを呼び出すと、マウスボタンが離されるか、document.releaseCapture()が呼び出されるまで、すべてのマウスイベントをこの要素にリターゲットします。"><code>element.setCapture()</code></a> および<a href="/ja/docs/Web/API/Document/releaseCapture" title="releaseCapture() メソッドは、この文書内の要素で現在有効になっているマウスキャプチャを解放します。要素におけるマウスキャプチャの有効化は element.setCapture() を呼び出すことで実行できます。"><code>document.releaseCapture()</code></a> メソッドが追加され、これらを用いることで、<code>指定要素で mousedown</code> イベントが発生した後にマウスが通常の追跡領域を越えても、マウスイベントを追い続けることができます。</li>
 <li>The <a href="/ja/docs/Web/API/Window/mozPaintCount" title="この window で現在の document が画面に描画された回数を返します。"><code>window.mozPaintCount</code></a> プロパティが追加されました。これを用いることで、何回ドキュメントが描画されたかを判定できます。これは Web アプリケーションのパフォーマンスをテストするときに役立ちます。</li>
 <li><a href="/ja/docs/Web/API/Window/navigator/appVersion" title="この項目についての文書はまだ書かれていません。書いてみませんか？"><code>window.navigator.appVersion</code></a> および <a href="/ja/docs/Web/API/Window/navigator/userAgent" title="この項目についての文書はまだ書かれていません。書いてみませんか？"><code>window.navigator.userAgent</code></a> から言語トークンが削除されました。代わりに <a href="/ja/docs/Web/API/Window/navigator/language" title="この項目についての文書はまだ書かれていません。書いてみませんか？"><code>window.navigator.language</code></a> もしくは <a href="/ja/docs/Content_negotiation">Accept-Language ヘッダ</a> を利用してください。 <a href="https://bugzilla.mozilla.org/show_bug.cgi?id=572656" title="FIXED: Remove the UI language from the UA string and navigator.appVersion">バグ 572656</a></li>
 <li><a href="/ja/docs/XMLHttpRequest">XMLHttpRequest</a> オブジェクトに追加された Gecko 固有の <code>mozResponseArrayBuffer </code>プロパティを用いると、レスポンスを文字列と同様 に JavaScript Typed Array として扱えます。</li>
 <li><a href="/ja/docs/DOM/Event/UIEvent/MouseEvent">Mouse イベント</a> に <code>mozPressure</code> プロパティが追加されました。このプロパティは圧力感知をサポートする入力デバイスでの圧力を示します。</li>
 <li><del>window.createBlobURL()</del> <ins><a href="/ja/docs/Web/API/Window/URL/createObjectURL" title="この項目についての文書はまだ書かれていません。書いてみませんか？"><code>window.URL.createObjectURL()</code></a></ins> および <a href="/ja/docs/Web/API/Window/URL/revokeObjectURL" title="この項目についての文書はまだ書かれていません。書いてみませんか？"><code>window.URL.revokeObjectURL()</code></a> メソッドを用いることで、ローカルファイルを参照する BLOB ("Binary Large OBject") URL を作成できます。</li>
 <li><a href="/ja/docs/Web/API/DOMImplementation/createHTMLDocument" title="この項目についての文書はまだ書かれていません。書いてみませんか？"><code>DOMImplementation.createHTMLDocument()</code></a> メソッドを用いることで、新しい HTML 文書を作成できます。</li>
 <li><a href="/ja/docs/Web/API/Node/mozMatchesSelector" title="この項目についての文書はまだ書かれていません。書いてみませんか？"><code>Node.mozMatchesSelector()</code></a> が指定セレクタ文字列が妥当ではない場合に正しくない <code>false</code> を返すのではなく、<code>SYNTAX_ERR</code> 例外を投げるようになりました。</li>
 <li>CSS 同様の省略構文を用いて 要素の SVG プロパティの値を設定できるようになりました。例: <code>element.style.fill = 'lime'</code>。詳細は <a href="/ja/docs/Web/API/Element/style" title="この項目についての文書はまだ書かれていません。書いてみませんか？"><code>element.style</code></a> を参照してください。</li>
 <li>ドキュメントルートに <a href="/ja/docs/Supporting_private_browsing_mode#Detecting_whether_private_browsing_mode_is_permanent"><code>privatebrowsingmode</code> 属性</a> が追加されました。これはプライベートブラウジングがセッションで一時的であるか永続的であるかの状態を含む、プライベートブラウジングモードの状態を示します。</li>
 <li><a href="/ja/docs/Web/API/Window/getComputedStyle" title="window.getComputedStyle() メソッドは、要素に適用されたスタイルの値を基本的な値に計算し直した後、すべてのCSSプロパティの値を返します。"><code>window.getComputedStyle()</code></a> メソッドの 2 番目のパラメータが、他の主なブラウザと同様に省略可能になりました。</li>
 <li>DOM の <a href="/ja/docs/DOM/event/StorageEvent"><code>StorageEvent</code></a> オブジェクトが仕様の最新版に合致するようになりました。</li>
 <li><a href="/ja/docs/Web/API/Window/setTimeout" title="この項目についての文書はまだ書かれていません。書いてみませんか？"><code>window.setTimeout()</code></a> メソッドの最小遅延時間を設定するための <code>dom.min_timeout_value が追加されました。</code></li>
 <li><a href="/ja/docs/Gecko-Specific_DOM_Events#MozAfterPaint"><code>MozAfterPaint</code></a> イベントは、潜在的なセキュリティ問題があるため、デフォルトでは送られなくなりました。設定を変更することで有効にできます。</li>
</ul>

<h3 id="Security" name="Security">セキュリティ</h3>

<dl>
 <dt><a href="/ja/docs/Introducing_Content_Security_Policy">Content Security Policy (CSP)</a></dt>
 <dd>Content Security Policy (CSP) は Mozilla が提案する Web デザイナーとサーバー管理者が Web サイトの相互利用でどのようなコンテンツを指定するかの仕様です。目的はクロスサイトスクリプティングを含む攻撃とデータインジェクション攻撃を判定し、軽減することです。</dd>
 <dt><a href="/ja/docs/Security/HTTP_Strict_Transport_Security">HTTP Strict Transport Security</a></dt>
 <dd>HTTP Strict Transport Security は Web サイトがブラウザに HTTP を用いる代わりに HTTPS を用いてのみやり取りすべきであることを伝えるセキュリティ機能です。</dd>
 <dt><a href="/ja/docs/The_X-FRAME-OPTIONS_response_header">X-FRAME-OPTIONS レスポンスヘッダ</a></dt>
 <dd>Internet Explorer 8 で導入された X-FRAME-OPTIONS HTTP レスポンスヘッダが Firefox でサポートされるようになりました。これを用いることでサイトがページをフレーム内で用いることができるかどうか、フレーム内で利用可能ならば、同じドメイン内に限定するかどうかを指示することができます。</dd>
 <dt><a href="/ja/docs/User_Agent_Strings_Reference">User Agent 文字列</a> の変更</dt>
 <dd><a class="link-https" href="https://bugzilla.mozilla.org/show_bug.cgi?id=572650">HTTP リクエストで送ったデータとエントロピーの総量を減少させるべき</a>にあるように、 ユーザエージェント文字列から暗号の強度を表す文字列と言語を表す文字列が削除されました。</dd>
</dl>

<h3 id="JavaScript" name="JavaScript">JavaScript</h3>

<p>JavaScript 1.8.5 で実装される変更の概要については、<a href="/ja/docs/New_in_JavaScript_1.8.5">JavaScript 1.8.5の新機能</a> を参照してください。Firefox 4 における JavaScript は ECMASCript 5 標準へのさらなる順守となる予定です。</p>

<h3 id="Developer_tools" name="Developer_tools">開発者ツール</h3>

<dl>
 <dt><a href="/ja/docs/Using_the_Web_Console">Web コンソールの利用</a></dt>
 <dd>Web コンソールツールは Web 開発者および拡張開発者のデバッグ作業の補助に役立ちます。</dd>
</dl>

<div class="geckoVersionNote">
<div class="geckoVersionHeading">
Gecko 2.0 note
<div style="font-size: 9px; line-height: 1; font-style: italic;">(Firefox 4 / Thunderbird 3.3 / SeaMonkey 2.1)</div>
</div>

<p>エラーコンソールは Firefox 4 からデフォルトで無効化されます。<code>devtools.errorconsole.enabled 設定を</code> <code>true</code> に変更し、ブラウザを再起動することで再び有効にすることができます。</p>
</div>

<h2 id="Changes_for_Mozilla_and_add-on_developers" name="Changes_for_Mozilla_and_add-on_developers">Mozilla およびアドオン開発者向けの変更</h2>

<p>Firefox 4 向けに既存の拡張を更新する上で役立つ Tips は、<a href="/ja/docs/Extensions/Updating_extensions_for_Firefox_4">Updating extensions for Firefox 4</a> を参照してください。ここでは既存のアドオンの互換性を破壊する主な変更点のいくつかを取り上げているだけです。ですから、上記記事も必ず読んでください。</p>

<p>テーマ開発者であるならば、注意する必要がある重要な変更点を理解するために <a href="/ja/docs/Theme_changes_in_Firefox_4">Theme changes in Firefox 4</a> を読むべきです。</p>

<h3 id="New_JavaScript_code_modules" name="New_JavaScript_code_modules">新しいJavaScript コードモジュール</h3>

<dl>
 <dt><a href="/ja/docs/JavaScript_code_modules/Services.jsm">Services.jsm</a></dt>
 <dd><code>Services.jsm</code> コードモジュールは preferences service や window mediator などのよく用いられているサービスへの参照を簡単に取得できるようにするゲッターを提供します。</dd>
 <dt><a href="/ja/docs/JavaScript_code_modules/ctypes.jsm">JS-ctypes API</a></dt>
 <dd>JS-ctypes API は C 互換外部ライブラリ関数を XPCOM を利用すること無しに呼び出せるようにします。</dd>
 <dt><a href="/ja/docs/Addons/Add-on_Manager">Add-ons Manager</a></dt>
 <dd>新しい Add-ons Manager はインストールされたアドオンについての情報の提供、それらの管理のためのサポート、および、アドオンのインストールと削除の方法を提供します。</dd>
 <dt><a href="/ja/docs/JavaScript_code_modules/PopupNotifications.jsm">PopupNotifications.jsm</a></dt>
 <dd>新しいポップアップ通知モジュールを用いることで簡単に魅力的な非モーダルな通知をユーザに提供できます。この API の使い方は<a href="/ja/docs/Using_popup_notifications">ポップアップ通知の利用</a>で参照できます。</dd>
 <dt><a href="/ja/docs/JavaScript_code_modules/Using#Locating_the_code_module">chrome: URL からコードモジュールを読み込む</a></dt>
 <dd><strong>chrome:</strong> URL を用いて JavaScript コードモジュールを読め込むことができるようになりました。JAR ファイルの中でも可能です。</dd>
 <dt>DownloadLastDir.jsm</dt>
 <dd><a href="/ja/docs/JavaScript_code_modules/DownloadLastDir.jsm"><code>DownloadLastDir.jsm</code></a> コードモジュールは <code>gDownloadLastDir</code> グローバル変数を提供します。この変数には最後のダウンロードが行われたディレクトリのパスを知るために利用可能な文字列が含まれています。このモジュールはプライベートブラウジングに対応しています。</dd>
 <dt><a href="/ja/docs/Performance/Measuring_performance_using_the_PerfMeasurement.jsm_code_module">PerfMeasurement.jsm コードモジュールを用いたパフォーマンスの測定</a></dt>
 <dd><a href="/ja/docs/JavaScript_code_modules/PerfMeasurement.jsm"><code>PerfMeasurement.jsm</code></a> コードモジュールは JavaScript コードにおける CPU レベルでのパフォーマンスデータを測定するための API を提供します。</dd>
</dl>

<h4 id="Miscellaneous_changes_to_code_modules" name="Miscellaneous_changes_to_code_modules">小さなコードモジュールの変更</h4>

<ul>
 <li><code>NetUtil.jsm</code> コードモジュールが <a href="/ja/docs/JavaScript_code_modules/NetUtil.jsm#readInputStreamToString()"><code>readInputStreamToString()</code></a> メソッドを提供するようになりました。これを用いることで、ストリームが null 文字を含んでいても、ストリームから文字列に任意のバイトを読み出せます。</li>
 <li><a href="/ja/docs/JavaScript_code_modules/Using_workers_in_JavaScript_code_modules">JavaScript コードモジュール内で Worker を利用</a>できるようになりました。</li>
</ul>

<h3 id="DOM_changes" name="DOM_changes">DOM の変更</h3>

<dl>
 <dt><a href="/ja/docs/Web/API/ChromeWorker" title="この項目についての文書はまだ書かれていません。書いてみませんか？"><code>ChromeWorker</code></a></dt>
 <dd>特権コード向けの新しいタイプの Worker です。これを用いると、拡張およびアプリケーションコードで Worker から <a href="/ja/docs/js-ctypes">js-ctypes</a> のようなものを用いることができます。</dd>
 <dt><a href="/ja/docs/DOM/Touch_events">タッチイベント</a></dt>
 <dd>(非標準の) タッチイベントのサポートが追加されました。これを用いると、タッチスクリーン上で同時に複数の指でトラックできます。</dd>
</dl>

<h3 id="XUL" name="XUL">XUL</h3>

<h4 id="Changes_to_the_tabbrowser_element" name="Changes_to_the_tabbrowser_element">Tabbrowser (gBrowser) の変更</h4>

<p>いくつかの変更が &lt;tabbrowser&gt; 要素になされており、タブ機能の拡張に影響があります。アイコンタブのサポートに加えて、タブバーが標準ツールバーに統合されたという変更もあります。この変更によって、ユーザがツールバーボタンをそこへドラッグできるようになっています。</p>

<ul>
 <li>TabClose/TabSelect/TabOpen イベントはもはや tabbrowser 要素 (gBrowser) にバブルアップしません。これらのイベントのためのイベントリスナーは gBrowser 直接ではなく gBrowser.tabContainer に追加すべきです。</li>
 <li>タブコンテキストメニューはもはや tabbrowser の無名の子要素ではありません。それゆえ <a href="/ja/docs/XUL_Overlays">XUL オーバーレイ</a>で直接オーバレイできるようになります。gBrowser.tabContextMenu 経由で JavaScript でより直接的にアクセスすることもできます。詳細は<a href="http://www.gavinsharp.com/blog/2010/03/31/accessingmodifying-the-firefox-tab-context-menu-from-extensions/">このブログ投稿</a>を参照してください。</li>
 <li>新たに <code><span><a href="/ja/docs/XUL/Property/visibleTabs">visibleTabs</a></span></code> プロパティが追加され、これを用いると、現在表示されているタブの配列を取得することができます。このことにより、現在のタブセットでどのタブが表示されているかを知ることができます。これは例えば、Firefox Panorama で利用されています。</li>
 <li>新たに <span id="m-showOnlyTheseTabs"><code><a href="/ja/docs/Mozilla/Tech/XUL/Method/showOnlyTheseTabs">showOnlyTheseTabs</a></code></span> メソッドが追加されました。これは Firefox Panorama で用いられています。</li>
 <li>新たに <span id="m-getIcon"><code><a href="/ja/docs/Mozilla/Tech/XUL/Method/getIcon">getIcon</a></code></span> メソッドが追加されました。これを用いると、<code><a href="/ja/docs/Mozilla/Tech/XUL/browser">&lt;xul:browser&gt;</a></code> 要素から引っ張り出す必要無しに、 タブのファビコンを得ることができます。</li>
 <li>新たに <code><span><a href="/ja/docs/XUL/Property/tabbrowser.tabs">tabbrowser.tabs</a></span></code> プロパティが追加されました。これを用いると、簡単に <code><a href="/ja/docs/Mozilla/Tech/XUL/tabbrowser">&lt;xul:tabbrowser&gt;</a></code> 要素内のタブの一覧を取得できます。</li>
 <li>新たに <span id="m-pinTab"><code><a href="/ja/docs/Mozilla/Tech/XUL/Method/pinTab">pinTab</a></code></span> と <span id="m-unpinTab"><code><a href="/ja/docs/Mozilla/Tech/XUL/Method/unpinTab">unpinTab</a></code></span> メソッドが追加されました。これを用いると、タブのアイコン化およびタブのアイコン化の解除ができます（つまり、アイコンタブと通常タブを切り替えます）。</li>
 <li><span id="m-getTabModalPromptBox"><code><a href="/ja/docs/Mozilla/Tech/XUL/Method/getTabModalPromptBox">getTabModalPromptBox</a></code></span> メソッドと <code><a href="/ja/docs/Mozilla/Tech/XUL/tabbrowser">&lt;xul:tabbrowser&gt;</a></code> 要素の <code id="a-tabmodalPromptShowing"><a href="/ja/docs/Mozilla/Tech/XUL/Attribute/tabmodalPromptShowing">tabmodalPromptShowing</a></code> 属性がタブモーダルアラートのサポートのために追加されました。</li>
</ul>

<h4 id="Changes_to_popups" name="Changes_to_popups">ポップアップに対する変更点</h4>

<ul>
 <li><code><a href="/ja/docs/Mozilla/Tech/XUL/popup">&lt;xul:popup&gt;</a></code> 要素がサポートされなくなりました。代わりに <code><a href="/ja/docs/Mozilla/Tech/XUL/menupopup">&lt;xul:menupopup&gt;</a></code> 要素を使うべきです。(<code>popup</code> 要素を用い続けた場合、その要素にはもはや何の特別な意味もないため、不具合に遭遇するでしょう。例えば、<code><a href="/ja/docs/Mozilla/Tech/XUL/menuseparator">&lt;xul:menuseparator&gt;</a></code> 要素は <code><a href="/ja/docs/Mozilla/Tech/XUL/popup">&lt;xul:popup&gt;</a></code> 要素内で用いたときに透明で表示される可能性があります。)</li>
 <li><code><a href="/ja/docs/Mozilla/Tech/XUL/menupopup">&lt;xul:menupopup&gt;</a></code> XUL 要素に <code><span><a href="/ja/docs/XUL/Property/triggerNode">triggerNode</a></span></code> プロパティが追加されました。このプロパティはポップアップを開くイベントが起こったノードを示します。これは <span id="m-openPopup"><code><a href="/ja/docs/Mozilla/Tech/XUL/Method/openPopup">openPopup</a></code></span> メソッドに対するトリガーイベント引数の追加も必要とします。また、 <code><span><a href="/ja/docs/XUL/Property/anchorNode">anchorNode</a></span></code> プロパティも追加されました。このプロパティはポップアップが作成されたときに指定されたアンカーを返します。</li>
 <li><code><a href="/ja/docs/Mozilla/Tech/XUL/panel">&lt;xul:panel&gt;</a></code> 要素に <code id="a-fade"><a href="/ja/docs/Mozilla/Tech/XUL/Attribute/fade">fade</a></code> および <code id="a-flip"><a href="/ja/docs/Mozilla/Tech/XUL/Attribute/flip">flip</a></code> 属性が追加されました。これらの属性は新しい "arrow" スタイル通知パネルの挙動を設定するために用いられます。</li>
</ul>

<h4 id="Remote_XUL_support_removed" name="Remote_XUL_support_removed">リモート XUL サポートの削除</h4>

<p>リモート XUL <a class="link-https" href="https://bugzilla.mozilla.org/show_bug.cgi?id=546857">がサポートされなくなりました</a>。 これは HTTP を経由して供給される XUL ドキュメントにのみ影響します。 また、<code>dom.</code><code>allow_XUL_XBL_for_file</code> の設定を作成して、その値を <code>true に設定しない限り、</code><span class="nowiki"><code>file://</code></span> URL 形式を用いた XUL 文書の読み込みも行えなくなります。しかしながら、ホワイトリスト機能を用いることで、特定ドメインのリモート XUL を読み込むことを許可できます。<a class="link-https" href="https://addons.mozilla.org/en-US/firefox/addon/235281/">Remote XUL Manager 拡張</a> を用いると、このホワイトリストを管理できます。</p>

<h4 id="Miscellaneous_XUL_changes" name="Miscellaneous_XUL_changes">小さな XUL の変更</h4>

<ul>
 <li><code id="a-readonly"><a href="/ja/docs/Mozilla/Tech/XUL/Attribute/readonly">readonly</a></code> 属性がフィールドで正しく動作するようになりました。</li>
 <li><code><a href="/ja/docs/Mozilla/Tech/XUL/resizer">&lt;xul:resizer&gt;</a></code> 要素でウィンドウをリサイズする代わりにリサイズする要素を指定できる <code id="a-element"><a href="/ja/docs/Mozilla/Tech/XUL/Attribute/element">element</a></code> 属性を用いることができるようになりました。</li>
 <li><code><a href="/ja/docs/Mozilla/Tech/XUL/resizer">&lt;xul:resizer&gt;</a></code> 要素に <code id="a-resizer.type"><a href="/ja/docs/Mozilla/Tech/XUL/Attribute/resizer.type">type</a></code> 属性が追加され、これを用いることで、要素の変わりにウィンドウのリサイズグリップを指定し、ウィンドウのリサイズグリップが 2 度描画されることを防ぐことができます。</li>
 <li>"active" 属性は XUL ウィンドウでは設定されません。背景ウィンドウに異なるスタイルを指定するための新しい <a href="/ja/docs/Web/CSS/:-moz-window-inactive" title="この項目についての文書はまだ書かれていません。書いてみませんか？"><code>:-moz-window-inactive</code></a> 擬似クラスを利用してください。</li>
 <li><code id="a-emptytext"><a href="/ja/docs/Mozilla/Tech/XUL/Attribute/emptytext">emptytext</a></code> 属性は非推奨になりました。代わりに <code id="a-placeholder"><a href="/ja/docs/Mozilla/Tech/XUL/Attribute/placeholder">placeholder</a></code> を用いるべきです。</li>
 <li><code><a href="/ja/docs/Mozilla/Tech/XUL/popup">&lt;xul:popup&gt;</a></code> 要素はサポートされません。代わりに <code><a href="/ja/docs/Mozilla/Tech/XUL/menupopup">&lt;xul:menupopup&gt;</a></code> を持ちいるべきです。</li>
 <li><code><a href="/ja/docs/Mozilla/Tech/XUL/window">&lt;xul:window&gt;</a></code> 要素が <code id="a-accelerated"><a href="/ja/docs/Mozilla/Tech/XUL/Attribute/accelerated">accelerated</a></code> 属性を提供するようになりました。true の場合、ハードウェアレイヤーマネージャがウィンドウをアクセラレーションすることが許可されます。</li>
 <li><code><a href="/ja/docs/Mozilla/Tech/XUL/stack">&lt;xul:stack&gt;</a></code> 要素が <code id="a-bottom"><a href="/ja/docs/Mozilla/Tech/XUL/Attribute/bottom">bottom</a></code> と <code id="a-right"><a href="/ja/docs/Mozilla/Tech/XUL/Attribute/right">right</a></code> 要素をサポートするようになりました。</li>
 <li><code><a href="/ja/docs/Mozilla/Tech/XUL/tree">&lt;xul:tree&gt;</a></code> 要素での <code id="a-alternatingbackground"><a href="/ja/docs/Mozilla/Tech/XUL/Attribute/alternatingbackground">alternatingbackground</a></code> 属性はサポートされません。代わりに <a href="/ja/docs/Web/CSS/:-moz-tree-row" title="この項目についての文書はまだ書かれていません。書いてみませんか？"><code>:-moz-tree-row</code></a> 擬似クラスを利用できます。</li>
 <li>anonid chevronPopup を持っていたブックマークツールバーのオーバーフローボタンは無名になりました。それは PlacesChevron の id を持っています。</li>
 <li><code><a href="/ja/docs/Mozilla/Tech/XUL/tabs">&lt;xul:tabs&gt;</a></code> 要素に <code><span><a href="/ja/docs/XUL/Property/tabbox">tabbox</a></span></code> プロパティが追加されました。これは古い <code>_tabbox</code> プロパティを置き換えます。古い方のプロパティは非推奨です（そして決してドキュメント化されません）。</li>
 <li>XUL <code><a href="/ja/docs/Mozilla/Tech/XUL/window">&lt;xul:window&gt;</a></code> 要素に <code id="a-drawintitlebar"><a href="/ja/docs/Mozilla/Tech/XUL/Attribute/drawintitlebar">drawintitlebar</a></code> 属性が追加されました。この値が <code>true であれば、</code>ウィンドウのコンテント領域にはタイトルバーが含まれており、タイトルバー内に描画することを許可します。</li>
 <li>新たに <code>TabPinned</code> および <code>TabUnpinned</code> イベントが追加され、これを用いることで、<a href="/ja/docs/Code_snippets/Tabbed_browser#Notification_when_a_tab_is_pinned_or_unpinned">タブがアイコン化したかアイコン化が解除されたかを検知できます</a>。</li>
 <li>新しい <a href="/ja/docs/Code_snippets/Tabbed_browser#Notification_when_a_tab%27s_attributes_change"><code>TabAttrModified</code> イベント</a> はタブの <code id="a-label"><a href="/ja/docs/Mozilla/Tech/XUL/Attribute/label">label</a></code>、<code id="a-crop"><a href="/ja/docs/Mozilla/Tech/XUL/Attribute/crop">crop</a></code>、<code id="a-busy"><a href="/ja/docs/Mozilla/Tech/XUL/Attribute/busy">busy</a></code>、 <code id="a-image"><a href="/ja/docs/Mozilla/Tech/XUL/Attribute/image">image</a></code>、あるいは、<code id="a-selected"><a href="/ja/docs/Mozilla/Tech/XUL/Attribute/selected">selected</a></code> 属性のいずれかが変化したときに送られます。</li>
 <li><code><a href="/ja/docs/Mozilla/Tech/XUL/tab">&lt;xul:tab&gt;</a></code> 要素に <code id="a-pinned"><a href="/ja/docs/Mozilla/Tech/XUL/Attribute/pinned">pinned</a></code> 属性が追加されました。これを用いることで、タブが現在アイコン化されているかどうか判定できます。</li>
 <li><code><a href="/ja/docs/Mozilla/Tech/XUL/tree">&lt;xul:tree&gt;</a></code> 要素上の <code>setDirectionIndicator</code> クラスは何もしないことがありましたが、一切利用されないようになりました。</li>
 <li><code><a href="/ja/docs/Mozilla/Tech/XUL/window">&lt;xul:window&gt;</a></code> 要素に <code id="a-chromemargin"><a href="/ja/docs/Mozilla/Tech/XUL/Attribute/chromemargin">chromemargin</a></code> 属性が追加され、これを用いることで、ウィンドウの両端のChrome とコンテントのマージンを設定できます。例えば、タイトルバーに描画するためにこれを用いることができます。</li>
 <li><code><a href="/ja/docs/Mozilla/Tech/XUL/window">&lt;xul:window&gt;</a></code> 要素に <code id="a-disablechrome"><a href="/ja/docs/Mozilla/Tech/XUL/Attribute/disablechrome">disablechrome</a></code> 属性が追加されました。これは <code>about:addons のように</code>ブラウザ内 UI に表示するために用いるときにウィンドウで Chrome のほどんどを隠すために用いることができます。</li>
 <li><code><a href="/ja/docs/Mozilla/Tech/XUL/window">&lt;xul:window&gt;</a></code> 要素に <code id="a-disablefastfind"><a href="/ja/docs/Mozilla/Tech/XUL/Attribute/disablefastfind">disablefastfind</a></code> 属性が追加されました。これを用いることで、ウィンドウ内のページ内検索バーを無効にできます。このときコンテント内でページ検索バーはサポートされません。例えば、これはアドオンパネルで使われています。</li>
 <li>ツールバーをツールボックスの外部に置けるようになりました。<code><a href="/ja/docs/Mozilla/Tech/XUL/toolbar">&lt;xul:toolbar&gt;</a></code> 要素の <code><span><a href="/ja/docs/XUL/Property/toolboxid">toolboxid</a></span></code> プロパティを設定することで、以前のように <code><a href="/ja/docs/Mozilla/Tech/XUL/toolbox">&lt;xul:toolbox&gt;</a></code> 要素のメンバーとして扱うことができます。また、<code><a href="/ja/docs/Mozilla/Tech/XUL/toolbox">&lt;xul:toolbox&gt;</a></code> 要素に <code><span><a href="/ja/docs/XUL/Property/externalToolbars">externalToolbars</a></span></code> プロパティが追加されました。このプロパティによって、そのツールボックスのメンバーとして扱われるツールバーのすべての一覧を取得できます。</li>
 <li>デバッグ目的向けに <a href="/ja/docs/XUL/Template_Guide/Template_Logging">logging XUL テンプレートのロギング</a> のサポートが追加されました。</li>
</ul>

<h3 id="UI_changes_affecting_developers" name="UI_changes_affecting_developers">開発者に影響がある UI の変更</h3>

<dl>
 <dt><a href="/ja/docs/The_add-on_bar">アドオンバー</a></dt>
 <dd>ステータスバーが削除され、新しいアドオンバーに置き換えられました。以前にステータスバーに UI を追加していた拡張は更新する必要があります。</dd>
 <dt><a href="/ja/docs/Hiding_browser_chrome">ブラウザのクロームを隠す</a></dt>
 <dd>ブラウザのクロームを隠したいときに、隠せるようになりました。例えば、<code>about:addons</code> がこれを用いています。</dd>
</dl>

<h3 id="Storage" name="Storage">Storage</h3>

<h4 id="Miscellaneous_storage_API_changes" name="Miscellaneous_storage_API_changes">小さなストレージ API の変更</h4>

<ul>
 <li><code><a href="/ja/docs/Mozilla/Tech/XPCOM/Reference/Interface/mozIStorageBindingParamsArray" title="">mozIStorageBindingParamsArray</a></code> インタフェースが 配列である<code><a href="/ja/docs/Mozilla/Tech/XPCOM/Reference/Interface/mozIStorageBindingParams" title="">mozIStorageBindingParams</a></code> オブジェクトの数を示す length 属性を持つようになりました。</li>
 <li><code><a href="/ja/docs/Mozilla/Tech/XPCOM/Reference/Interface/mozIStorageStatement " title="">mozIStorageStatement </a></code> の メソッド <a href="/ja/docs/mozIStorageStatemt#bindPrameters">bindParameters</a> が 指定された <code><a href="/ja/docs/Mozilla/Tech/XPCOM/Reference/Interface/mozIStorageBindingParamsArray" title="">mozIStorageBindingParamsArray</a></code> が空のときにエラーを返すようになりました。</li>
 <li><code><a href="/ja/docs/XPCOM_Interface_Reference/mozIStorageConnection#clone()">mozIStorageConnection.clone()</a></code> メソッドが追加されました。これを用いると、存在するデータベース接続を複製できます。</li>
 <li><code><a href="/ja/docs/XPCOM_Interface_Reference/mozIStorageConnection#asyncClose()">mozIStorageConnection.asyncClose()</a></code> が追加されました。これを用いると、非同期にデータベース接続を閉じることができます。クローズ処理が完了したときに通知されるコールバックを指定します。</li>
 <li><code><a href="/ja/docs/XPCOM_Interface_Reference/mozIStorageConnection#setGrowthIncrement()">mozIStorageConnection.setGrowthIncrement()</a></code> メソッドが追加されました。これを用いると、SQLite のフラグメンテーションを減らすことを助けるために、データベースファイルでの一度の増加量を指定できます。</li>
 <li><code>SQLITE_CONSTRAINT</code> エラーが <code>NS_ERROR_FAILURE</code> の代わりに <code>NS_ERROR_STORAGE_CONSTRAINT</code> を報告するようになりました。</li>
</ul>

<h3 id="XPCOM" name="XPCOM">XPCOM</h3>

<p>以下から参照できる特定の変更に加えて、凍結されたインタフェースが一切無くなったという重要な変更もあります。すべてのインタフェースは非凍結となっています。ドキュメンテーションに書いていることに関わらずです。ドキュメンテーションを後ほど更新する予定です。</p>

<dl>
 <dt><a href="/ja/docs/XPCOM/XPCOM_changes_in_Gecko_2.0">Gecko 2.0 における XPCOM の変更</a></dt>
 <dd>Firefox 4 で互換性に影響を与える XPCOM への変更についての詳細。</dd>
 <dt><a href="/ja/docs/Components.utils.getGlobalForObject">Components.utils.getGlobalForObject()</a></dt>
 <dd>この新しいメソッドはオブジェクトが属しているグローバルオブジェクトを返します。これは現在削除された <code>__parent__ の一般的用途を置き換えます。</code></dd>
</dl>

<h3 id="Places" name="Places">Places</h3>

<ul>
 <li>Places クエリの結果が複数のオブザーバによって提供されるようになり、それらのクエリは非同期で実行される可能性があります。このことにより、<code><a href="/ja/docs/Mozilla/Tech/XPCOM/Reference/Interface/nsINavHistoryResult" title="">nsINavHistoryResult</a></code>、<code><a href="/ja/docs/Mozilla/Tech/XPCOM/Reference/Interface/nsINavHistoryQueryOptions" title="">nsINavHistoryQueryOptions</a></code>、および<code><a href="/ja/docs/Mozilla/Tech/XPCOM/Reference/Interface/nsINavHistoryContainerResultNode" title="">nsINavHistoryContainerResultNode</a></code> インタフェースにいくつかの変更があります。より大きな変更は、<code><a href="/ja/docs/Mozilla/Tech/XPCOM/Reference/Interface/nsINavHistoryResultViewer" title="">nsINavHistoryResultViewer</a></code> インタフェースが <code><a href="/ja/docs/Mozilla/Tech/XPCOM/Reference/Interface/nsINavHistoryResultObserver" title="">nsINavHistoryResultObserver</a></code> に改名されたことです。</li>
 <li>いくつかの <a href="/ja/docs/Observer_Notifications#Places">新しい通知</a> が追加されました。この通知を用いると、ブラウザが Places サービスのシャットダウンプロセスをより確実に追跡できます。これらのうち、ほとんどは内部での利用のためにのみ用意されたものですが、<code>places-connection-closed</code> 通知は Places サービスが自身のシャットダウンプロセスを完了したときを知るために利用可能です。</li>
 <li>いくつかの Places のメソッドで配列サイズ出力を指定する引数がオプションになりました。</li>
 <li><code>&lt;menupopup type="places"&gt;</code> のサポートが削除されました。代わりに、以前は自動で行なわれていた Places の情報を持つメニューを手動で作成して配置する必要があります。詳細は<a href="/ja/docs/Displaying_Places_information_using_views#Menu_view">メニュービューを用いて Places 情報を表示する</a>を参照してください。</li>
</ul>

<h3 id="Interface_changes" name="Interface_changes">インタフェースの変更</h3>

<ul>
 <li>The <code><a href="/ja/docs/XPCOM_Interface_Reference/nsIDocShell">nsIDocShell</a></code> and <code><a href="/ja/docs/XPCOM_Interface_Reference/nsIWebBrowser">nsIWebBrowser</a></code> interfaces now have a new <code>isActive</code> attribute, which is used to allow optimization of code paths for documents that aren't currently visible.</li>
 <li>The <code><a href="/ja/docs/XPCOM_Interface_Reference/nsIMemory">nsIMemory</a></code> method <code><a href="/ja/docs/en-US/XPCOM_Interface_Reference/nsIMemory#isLowMemory()">nsIMemory.isLowMemory()</a></code> has been deprecated. You should use <a href="/ja/docs/XPCOM_Interface_Reference/nsIMemory#Low_memory_notifications">"memory-pressure" notifications</a> to watch for low memory situations instead.</li>
 <li>The API for handling redirects on HTTP channels has changed to let them be processed asynchronously. Any code that implements redirect handling using <code><a href="/ja/docs/en-US/XPCOM_Interface_Reference/nsIChannelEventSink#onChannelRedirect()">nsIChannelEventSink.onChannelRedirect()</a></code> needs to be updated to use <code><a href="/ja/docs/en-US/XPCOM_Interface_Reference/nsIChannelEventSink#asyncOnChannelRedirect()">nsIChannelEventSink.asyncOnChannelRedirect()</a></code> instead. This accepts a callback handler that must be called when a redirect is successfully completed.</li>
 <li>The <code><a href="/ja/docs/en-US/XPCOM_Interface_Reference/nsINavHistoryResultObserver#batching()">nsINavHistoryResultObserver.batching()</a></code> method has been added, providing a way to group Places operations into batches, reducing the number of update notifications delivered, which can improve performance when observers are performing relatively involved tasks (such as refreshing views).</li>
 <li>The long-obsolete <code>nsIPref</code> interface has finally been removed. If you haven't already switched to <code><a href="/ja/docs/XPCOM_Interface_Reference/nsIPrefService">nsIPrefService</a></code>, now is the time.</li>
 <li>The <code><a href="/ja/docs/XPCOM_Interface_Reference/nsISessionStore">nsISessionStore</a></code> and <code><a href="/ja/docs/XPCOM_Interface_Reference/nsISessionStartup">nsISessionStartup</a></code> interfaces received changes to support on-demand session restore. See the <code><a href="/ja/docs/en-US/XPCOM_Interface_Reference/nsISessionStore#restoreLastSession()">nsISessionStore.restoreLastSession()</a></code> method.</li>
 <li>The <code><a href="/ja/docs/XPCOM_Interface_Reference/nsIPrincipal">nsIPrincipal</a></code> methods <code><a href="/ja/docs/en-US/XPCOM_Interface_Reference/nsIPrincipal#subsumes()">nsIPrincipal.subsumes()</a></code> and <code><a href="/ja/docs/en-US/XPCOM_Interface_Reference/nsIPrincipal#checkMayLoad()">nsIPrincipal.checkMayLoad()</a></code>, as well as its <code>origin</code>, <code>csp</code>, and <code>URI</code> attributes, are now available from script; previously they were only available from native code.</li>
 <li>The <code><a href="/ja/docs/XPCOM_Interface_Reference/nsIPrompt">nsIPrompt</a></code> interface now supports tab-modal alerts; see <a href="/ja/docs/Using_tab-modal_prompts">Using tab-modal prompts</a> for details.</li>
 <li>The <code><a href="/ja/docs/en-US/XPCOM_Interface_Reference/nsIEffectiveTLDService#getPublicSuffixFromHost()">nsIEffectiveTLDService.getPublicSuffixFromHost()</a></code> method now correctly rejects host name starting with a period (".").</li>
 <li>The <code><a href="/ja/docs/en-US/XPCOM_Interface_Reference/mozIJSSubScriptLoader#loadSubScript()">mozIJSSubScriptLoader.loadSubScript()</a></code> method now has an optional argument allowing you to specify the character set of the script; if one is not provided, ASCII is assumed (as was always assumed previously).</li>
 <li>The <code>nsIAccessProxy</code> interface has been removed. It was an implementation detail that has outlived its usefulness.</li>
 <li>The <code><a href="/ja/docs/XPCOM_Interface_Reference/nsIContentView">nsIContentView</a></code> and <code><a href="/ja/docs/XPCOM_Interface_Reference/nsIContentViewManager">nsIContentViewManager</a></code> interfaces have been added for Firefox Mobile. It represents a scrollable content view whose contents are actually drawn by a separate process.</li>
 <li>The <code><a href="/ja/docs/XPCOM_Interface_Reference/nsIDiskCacheStreamInternal">nsIDiskCacheStreamInternal</a></code> interface has been added.</li>
 <li>The <code><a href="/ja/docs/XPCOM_Interface_Reference/nsIExternalURLHandlerService">nsIExternalURLHandlerService</a></code> interface has been added.</li>
 <li>The <code><a href="/ja/docs/XPCOM_Interface_Reference/nsISyncJPAKE">nsISyncJPAKE</a></code> interface has been added. See <a href="https://bugzilla.mozilla.org/show_bug.cgi?id=601645">bug 601645</a>.</li>
</ul>

<ul>
 <li><code><a href="/ja/docs/Mozilla/Tech/XPCOM/Reference/Interface/nsIDocShell" title="">nsIDocShell</a></code> および <code><a href="/ja/docs/Mozilla/Tech/XPCOM/Reference/Interface/nsIWebBrowser" title="">nsIWebBrowser</a></code> インタフェースに新しく <code>isActive</code> 属性が追加されました。これは現在表示されていないドキュメントのためにコードパスを最適化することを許可するために用いることができます。</li>
 <li><code><a href="/ja/docs/Mozilla/Tech/XPCOM/Reference/Interface/nsIMemory" title="">nsIMemory</a></code> のメソッドである <a href="/ja/docs/XPCOM_Interface_Reference/nsIMemory/isLowMemory"><code>isLowMemory()</code></a> は非推奨になりました。低メモリ状況を監視するには <a href="/ja/docs/XPCOM_Interface_Reference/nsIMemory#Low_memory_notifications">"memory-pressure" 通知</a> を用いることが推奨されます。</li>
 <li>HTTP チャンネル上でリダイレクトを扱う API が非同期で動作できるように変更されました。<code><a href="/ja/docs/XPCOM_Interface_Reference/nsIChannelEventSink#onChannelRedirect()">nsIChannelEventSink.onChannelRedirect()</a></code> を用いてリダイレクトを扱う実装を行なっているコードは <code>nsIChannelEventSink.asyncOnChannelRedirect</code> を代わりに用いて更新する必要があります。これはリダイレクトが正常に完了したときに呼び出されるコールバックハンドラを受け入れます。</li>
 <li><code><a href="/ja/docs/XPCOM_Interface_Reference/nsINavHistoryResultObserver#batching()">nsINavHistoryResultObserver.batching()</a></code> メソッドが追加されました。このメソッドは Places 操作をバッチにグループ化する方法を提供し、送られてくる更新通知の数を減少させ、その結果、オブザーバが（ビューをリフレッシュするような）相対的にタスクを追加するときのパフォーマンスを向上させます。</li>
 <li>長い間廃止状態であった <code><a href="/ja/docs/Mozilla/Tech/XPCOM/Reference/Interface/nsIPref" title="">nsIPref</a></code> インタフェースがついに削除されました。まだ <code><a href="/ja/docs/Mozilla/Tech/XPCOM/Reference/Interface/nsIPrefService" title="">nsIPrefService</a></code> に移行していないなら、今がそのときです。</li>
 <li><code><a href="/ja/docs/Mozilla/Tech/XPCOM/Reference/Interface/nsISessionStore" title="">nsISessionStore</a></code> および <code><a href="/ja/docs/Mozilla/Tech/XPCOM/Reference/Interface/nsISessionStartup" title="">nsISessionStartup</a></code> インタフェースがユーザの要求に応じたセッションリストアのサポートへの変更を受けとるようになりました。<code><a href="/ja/docs/XPCOM_Interface_Reference/nsISessionStore#restoreLastSession()">nsISessionStore.restoreLastSession()</a></code> メソッドを参照してください。</li>
 <li><code><a href="/ja/docs/Mozilla/Tech/XPCOM/Reference/Interface/nsIPrincipal" title="">nsIPrincipal</a></code> のメソッドである <code><a href="/ja/docs/XPCOM_Interface_Reference/nsIPrincipal#subsumes()">nsIPrincipal.subsumes()</a></code> および <code><a href="/ja/docs/XPCOM_Interface_Reference/nsIPrincipal#checkMayLoad()">nsIPrincipal.checkMayLoad()</a></code> が <code>origin</code>、<code>csp、</code> および <code>URI</code> 属性同様に、スクリプトから利用可能になりました。以前はこれらはネイティブコードからのみ利用可能でした。</li>
 <li><code><a href="/ja/docs/Mozilla/Tech/XPCOM/Reference/Interface/nsIPrompt" title="">nsIPrompt</a></code> インタフェースがタブモーダルアラートをサポートするようになりました。詳細は<a href="/ja/docs/Using_tab-modal_prompts">タブモーダルプロンプトの利用</a>を参照してください。</li>
 <li><code><a href="/ja/docs/XPCOM_Interface_Reference/nsIEffectiveTLDService#getPublicSuffixFromHost()">nsIEffectiveTLDService.getPublicSuffixFromHost()</a></code> メソッドがピリオド (".") で始まるホスト名を正しく拒否するようになりました。</li>
</ul>

<h3 id="Memory_management" name="Memory_management">メモリ管理</h3>

<dl>
 <dt><a href="/ja/docs/Infallible_memory_allocation">確実なメモリアロケーション</a></dt>
 <dd>Mozilla は null を返さないことを保証する確実なメモリアロケータを複数提供するようになりました。この記事を読んでそれらがどのように動作し、どのようにして不確実な、あるいは、確実なメモリアロケーションを明確に指定して呼び出すのかを学んでください。</dd>
</dl>

<h3 id="Other_changes" name="Other_changes">その他の変更</h3>

<ul>
 <li>Firefox 内に含まれるリソースのほとんどが単一の JAR アーカイブである <code>omni.jar</code> にまとめられました。これにより、 I/O が減少し、その結果、起動パフォーマンスが向上しています。詳細は <a href="/ja/docs/About_omni.jar">omni.jar について</a>を読んでください。</li>
 <li><code>accessibility.disablecache</code> 設定はサポートされなくなりました。これはデバッグ目的で公開されており、もはや用いられません。</li>
 <li>バージョンアップによって GUID が変更になるアドオンが正しく更新されるようになりました。</li>
 <li>プラットフォーム固有のディレクトリを削除した副作用として、各プラットフォーム向けに異なった設定を提供することができなくなりました。</li>
 <li>デフォルトで、拡張はインストール時に展開されなくなりました。その代わりに XPI ファイルから直接実行されます。拡張は古い挙動を選択するために<a href="/ja/docs/Install_Manifests">インストールマニフェスト</a>内で <a href="/ja/docs/Install_Manifests#unpack">unpack</a> プロパティを使用できます。バイナリコンポーネントや、<a href="/ja/docs/js-ctypes">js-ctypes</a> を利用して読み込まれる DLL、<a href="/ja/docs/Creating_OpenSearch_plugins_for_Firefox">検索プラグイン</a>、辞書、ウィンドウアイコンは展開される必要があるように指定しなければなりません。<a href="/ja/docs/XUL/School_tutorial/Local_Storage#SQLite">SQLite データベースを生成する</a>拡張や、拡張ディレクトリからファイルシステムへ相対的に何かをコピーする拡張も、それらのコードを変更する必要があるかもしれません。</li>
 <li>カスタマイズされた Firefox に<a href="/ja/docs/Developer_Guide/Customizing_Firefox#Including_extensions_with_your_distribution_of_Firefox">アプリケーションスタートアップ時に自動でインストールされる</a>拡張を含められるようになりました。</li>
</ul>

<h2 id="Other_changes_2" name="Other_changes_2">その他の変更</h2>

<dl>
 <dt>ルートの chrome.manifest ファイルだけが読み込まれるように</dt>
 <dd>ルートの <code>chrome.manifest</code> ファイルだけが読み込まれるようになりました。 2 つ以上のマニフェストファイルを読み込む必要がある場合は、ルートの <code>chrome.manifest</code> でそれらを読み込むために <a href="/ja/docs/Chrome_Registration#manifest"><code>manifest</code></a> コマンドを使用できます。</dd>
 <dt>Gopher サポートの削除</dt>
 <dd>Gopher プロトコルがネイティブでサポートされなくなりました。継続してサポートを受けるには <a class="link-https" href="https://addons.mozilla.org/addon/7685/">OverbiteFF</a> 拡張を利用できます。</dd>
 <dt><a href="/ja/docs/The_message_manager">コンテントプロセスイベントハンドリング</a></dt>
 <dd>out-of-process プラグインのサポートとその他の multiple-process 機能をサポートするために、プロセス間でメッセージを送ることをサポートするための新しい API が導入されました。</dd>
 <dt><a href="/ja/docs/Extensions/Bootstrapped_extensions">ブートストラップ拡張</a></dt>
 <dd>ブラウザを再起動せずにインストール、アンインストール、更新（またはダウングレード）できる拡張を作成できるようになりました。</dd>
 <dt>デフォルトプラグイン の削除</dt>
 <dd>デフォルトプラグインが削除されました。アプリケーションプラグインフォルダもデフォルトで削除されますが、このフォルダ経由でプラグインをインストールするためのサポートはまだ存在します。<a class="link-https" href="https://bugzilla.mozilla.org/show_bug.cgi?id=533891">bug 533891</a> を参照してください。</dd>
 <dt>Extension Manager の AddonManager への置き換え</dt>
 <dd><a href="/ja/docs/XPCOM_Interface_Reference/nsIExtensionManager">nsIExtensionManager</a> は <a href="/ja/docs/Addons/Add-on_Manager/AddonManager">AddonManager</a> に置き換えられました。 指定した拡張 ID からインストール場所を取得するための方法は現在のところ存在しないと思われるので、それに最も近い回避策はプロファイルディレクトリを見つけるためにディレクトリサービスを用い、それに "extensions" を追加することです（この手段ではプロファイルディレクトリ外あるいは他の位置にエイリアスされている拡張は取得できません）。</dd>
 <dt>子 HWND はもはや利用されません</dt>
 <dd>Firefox は Windows で内部利用していた 子 HWND を作成しないようになりました。これらの HWND を扱うネィティブコードを用いる拡張を書いていた場合、その拡張は Firefox 4 では動作しないでしょう。HWND を用いることを止めるか、<a href="/ja/docs/NPAPI">NPAPI</a> プラグインで HWND に依存するコードをラップする必要があります。それは多大な作業であり、HWND を直接用いることを避けられるならば、そうすべきです。</dd>
 <dt>ジェスチャの変更</dt>
 <dd>トラックパッド上の 3 本指の上下スワイプジェスチャが、デフォルトで、Firefox Panorama (旧称 TabCandy) の開閉に変更されました。これらの変更を以前の scroll-to-top および scroll-to-bottom コマンドに戻すには、about:config を開き、<code>browser.gesture.swipe.down</code> を <code>cmd_scrollBottom</code> にし、<code>browser.gesture.swipe.up</code> を <code>cmd_scrollTop</code> に設定してください。</dd>
</dl>

<h2 id="See_also" name="See_also">関連情報</h2>

<div><div class="multiColumnList">
<ul>
<li><a href="/ja/docs/Mozilla/Firefox/Releases/5">Firefox 5 for developers</a></li><li><a href="/ja/docs/Mozilla/Firefox/Releases/4">Firefox 4 for developers</a></li><li><a href="/ja/docs/Mozilla/Firefox/Releases/3.6">Firefox 3.6 for developers</a></li><li><a href="/ja/docs/Mozilla/Firefox/Releases/3.5">Firefox 3.5 for developers</a></li><li><a href="/ja/docs/Mozilla/Firefox/Releases/3">Firefox 3 for developers</a></li><li><a href="/ja/docs/Mozilla/Firefox/Releases/2">Firefox 2 for developers</a></li><li><a href="/ja/docs/Mozilla/Firefox/Releases/1.5">Firefox 1.5 for developers</a></li></ul>
</div></div>