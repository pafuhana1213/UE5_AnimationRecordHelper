# AnimationRecordHelper
TakeRecorderの各機能・設定を外部から呼び出したり、TakeRecorderによる録画結果（LevelSequence）をかんたんにプレビューできるようにすることで、モーションキャプチャなどの作業をより効率よく進めるために作成したプラグインです。
[![](https://img.youtube.com/vi/o-_-RsJBdWs/0.jpg)](https://www.youtube.com/watch?v=o-_-RsJBdWs)

# できること
- TakeRecorderによる録画開始・終了をキー・ボタン入力から行えます。エディタ操作は不要です
- TakeRecorderの録画結果のプレビューをキー・ボタン入力から行えます。エディタ操作は不要です
- VRM4UプラグインによるMocopi対応での利用を前提としたレベルを用意しています
   - LiveLinkFace対応済み
   - キー・ボタン入力による指の制御モーション再生
   
# エンジンバージョン
5.1

# 事前準備
1. Code -> Download Zipを押しプラグインをダウンロード  
![image](https://user-images.githubusercontent.com/8957600/213871666-212e8077-6485-4b85-a888-3addc87f7624.png)
2. ダウンロードしたデータを解凍し、中にあるPluginsフォルダをUE5プロジェクトのルートフォルダ（.uprojectがある階層）に配置

3. VRM4UプラグインによるMocopi対応用レベルを開きたい場合はVRM4Uプラグインを使う環境を構築する  
https://ruyo.github.io/VRM4U/  
TakeRecorder機能を呼び出す部分だけならVRM4Uプラグインの導入は必須ではありませんが、  
エラーが出ているノードの削除が必要かもしれません。なので、初心者の方はVRM4Uを導入したほうが混乱は少ないと思います。  
なお本プラグインは

# 基本的なつかいかた
1. Plugins/AnimationRecordHelper/Maps/ForMocopiレベルを開く  
![image](https://user-images.githubusercontent.com/8957600/213871595-73b01ee1-927f-43f7-b28b-0dde4bbfcf29.png)

2. レベル上のBP_MocopiReceiverをセットアップ
BP_MocopiReceiverのReceive IPAddressを自身のPCと同じIPアドレスに設定  
BP_MocopiReceiverのIPAddress Listが参考になります  
![image](https://user-images.githubusercontent.com/8957600/213872381-6e6b8af4-82d0-4520-8967-57f8406281e7.png)  
参考：https://ruyo.github.io/VRM4U/08_mocopi/

3. エディタを実行して、Mocopiの動きと連動していることを確認

# フェイシャルキャプチャ
LiveLinkFaceを使う環境を整えた後に、レベル上のBP_LiveLinkFaceにあるLive Link Subjectを適切なデバイスに設定してください
https://docs.unrealengine.com/5.0/ja/recording-face-animation-on-ios-device-in-unreal-engine/   
https://ruyo.github.io/VRM4U/05_tracking/  
