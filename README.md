# AI-ｽﾀｯｸﾁｬﾝ２　ナイトライダー　シーズン２
<br>
robo8080さん制作の「AIｽﾀｯｸﾁｬﾝ2」、motohさん制作の「AIｽﾀｯｸﾁｬﾝ２ Func-Call仕様」をベースに、<br>
機能を追加or削除した派生型のAIｽﾀｯｸﾁｬﾝ２です。M5Stack core2 とcore2AWSにて動作します。<br>
<br>
<br>
〇　特長<br>
<br>
・ファンクションコール機能を装備しました。通常の会話の他に、最新のニュースヘッドライン、日付や時間、天気予報にも応えることができます。<br>
・通信中は側面LEDがナイトライダーのフラッシャーのように、おしゃべり中はネコミミLEDがボイスインジケーターのようにそれぞれ点灯します（LEDはパーツは必須ではありません）。<br>
・ｽﾀｯｸﾁｬﾝが転んだときや強い衝撃を受けた時はナイトフラッシャーとともに音声で警告を促します。<br>
・ｽﾀｯｸﾁｬﾝに素早く大きな角速度を与えると（ドアノブ回す要領）、側面LEDが点灯、消灯します。<br>
<br>
<br>
〇　セッティング<br>
<br>
・基本的なセッティングはオリジナルのAIｽﾀｯｸﾁｬﾝ２と同一です。<br>
・マイクロSDカード内にwifi.textファイル、apikey.textファイルがあれば、その情報でネットに接続、chatGPTと通信を始めます。<br>
<br>
<br>
     　  wifi.txtファイル：ファイル名は"wifi.txt"で、中身は次の通りです。<br>
     　  YOUR_WIFI_SSID<br>
     　  YOUR_WIFI_PASS<br>
<br>
     　  apikey.txtファイル：ファイル名は"apikey.txt"で、中身は次の通りです。<br>
     　  OPENAI_API key<br>
    　   VOICEVOX_API key<br>
    　   Speach To Text_API key<br>
<br>
<br>
<br>
・ｽﾀｯｸﾁｬﾝの性格（ロール設定）や音量（ボリューム）、音声（話者）を変更するときはPCにて行います。<br>
 <br>
　　     ブラウザで"http://xxxx.xxxx.xxxx.xxxx/role"　にアクセスすると、ロールを設定できます。<br>
  　 　  (xxxx.xxxx.xxxx.xxxxはAIスタックチャン２の起動時に表示されるIPアドレスです。)<br>
  　 　  テキストエリアに何も入力せずに送信すると、以前に設定されたロールが削除されます。<br>
<br>
  　 　  また、"http://xxxx.xxxx.xxxx.xxxx/role_get"　にアクセスすると、現在設定しているロールを取得できます。<br>
<br>
　　　　　同様にボリュームを変更するときは"http://xxxx.xxxx.xxxx.xxxx/setting?volume=200"　の200の数値を0～255で調整してください。<br>
    <br>
　　　　　話者を変更するときも"http://xxxx.xxxx.xxxx.xxxx/setting?speaker=3"　の3の数値を変えてください。<br>

　　　
<br>
　　　　VoiceVox話者番号一覧<br>
　　　　0:四国めたん（あまあま）<br>
　　　　1:ずんだもん（あまあま）<br>
　　　　2:四国めたん（ノーマル）<br>
　　　　3:ずんだもん（ノーマル）<br>
　　　　4:四国めたん（セクシー）<br>
　　　　5:ずんだもん（セクシー）<br>
　　　　6:四国めたん（ツンツン）<br>
　　　　7:ずんだもん（ツンツン）<br>
　　　　8:春日部つむぎ（ノーマル）<br>
　　　　9:波音リツ（ノーマル）<br>
　　　　10:雨晴はう（ノーマル）<br>
　　　　11:玄野武宏（ノーマル）<br>
　　　　12:白上虎太郎（ふつう）<br>
　　　　13:青山龍星（ノーマル）<br>
　　　　14:冥鳴ひまり（ノーマル）<br>
　　　　15:九州そら（あまあま）<br>
　　　　16:九州そら（ノーマル）<br>
　　　　17:九州そら（セクシー）<br>
　　　　18:九州そら（ツンツン）<br>
　　　　19:九州そら（ささやき）<br>
　　　　20:もち子(cv 明日葉よもぎ)<br>
　　　　21:剣崎雌雄（ノーマル）<br>
　　　　22:ずんだもん（ささやき）<br>
　　　　23:WhiteCUL（ノーマル）<br>
　　　　24:WhiteCUL（たのしい）<br>
　　　　25:WhiteCUL（かなしい）<br>
　　　　26:WhiteCUL（びえーん）<br>
　　　　27:後鬼（人間ver.）<br>
　　　　28:後鬼（ぬいぐるみver.）<br>
　　　　29:No.7（ノーマル）<br>
　　　　30:No.7（アナウンス）<br>
　　　　31:No.7（読み聞かせ）<br>
　　　　32:白上虎太郎（わーい）<br>
　　　　33:白上虎太郎（びくびく）<br>
　　　　34:白上虎太郎（おこ）<br>
　　　　35:白上虎太郎（びえーん）<br>
　　　　36:四国めたん（ささやき）<br>
　　　　37:四国めたん（ヒソヒソ）<br>
　　　　38:ずんだもん（ヒソヒソ）<br>
　　　　39:玄野武宏（喜び）<br>
　　　　40:玄野武宏（ツンギレ）<br>
　　　　41:玄野武宏（悲しみ）<br>
　　　　42:ちび式じい（ノーマル）<br>
　　　　43:櫻歌ミコ（ノーマル）<br>
　　　　44:櫻歌ミコ（第二形態）<br>
　　　　45:櫻歌ミコ（ロリ）<br>
　　　　46:小夜/SAYO（ノーマル）<br>
　　　　47:ナースロボ＿タイプＴ（ノーマル）<br>
　　　　48:ナースロボ＿タイプＴ（楽々）<br>
　　　　49:ナースロボ＿タイプＴ（恐怖）<br>
　　　　50:ナースロボ＿タイプＴ（内緒話）<br>
　　　　51:†聖騎士 紅桜†（ノーマル）<br>
　　　　52:雀松朱司（ノーマル）<br>
　　　　53:麒ヶ島宗麟（ノーマル）<br>
　　　　54:春歌ナナ（ノーマル）<br>
　　　　55:猫使アル（ノーマル）<br>
　　　　56:猫使アル（おちつき）<br>
　　　　57:猫使アル（うきうき）<br>
　　　　58:猫使ビィ（ノーマル）<br>
　　　　59:猫使ビィ（おちつき）<br>
　　　　60:猫使ビィ（人見知り）<br>
    <br>
    <br>
    <br>
〇　天気予報の地域設定<br>
 <br>
・天気予報の情報はデフォルトでは関東（東京地方）になっております。<br>
・ その他の地域ではお手数ですがマイクロSDカード内にテキストファイルを用意して、都市ID(CityID)を入力してください(下記の例、140010は神奈川県のID）。<br>
    <br>
    ファイル名： weather_city_id.txt<br>
<br>
    140010<br>
     <br>
     各都市・地方のIDは、　https://weather.tsukumijima.net/primary_area.xml 　で調べてください。<br>
     <br>
     <br>

〇AIスタックチャンの操作方法<br>
<br>
・ｽﾀｯｸﾁｬﾝの額付近にタッチするとマイクからの録音が始まり音声認識で会話できるようになります。録音時間は５秒程度です。<br>
<br>
・ｽﾀｯｸﾁｬﾝの左端中央付近にタッチすると、独り言モードをON/OFFできます。<br>
<br>
・ｽﾀｯｸﾁｬﾝの画面中央付近にタッチすると首振り（サーボの動き）をON/OFFできます。<br>
<br>
・ｽﾀｯｸﾁｬﾝの右端中央付近にタッチすると、バッテリー残量を教えてくれます。<br>
<br>
<br>  
<br>
<br>
〇　注意事項<br>
    <br>
・スマホアプリの「ｽﾀｯｸﾁｬﾝconnect」には対応しておりません。会話時はｽﾀｯｸﾁｬﾝと直接してください。音量、性格（ロール）設定等もPCにて行ってください。<br>
・AIｽﾀｯｸﾁｬﾝ２プラスの「ウエイクワード」機能は装備しておりません。<br>
・時間や日付を応えてくれますが、タイマー機能は装備されておりません。<br>
　「3分経ったら教えて」「あす7時に起こして」といったオーダーは「分かりました」と言っても信用しないでください。<br>
　　
<br>

    

