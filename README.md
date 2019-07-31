# VRSampleをOculusQuestで動かす
OculusQuestのビルドテストを兼ねて、UnityのVRサンプルアセットをOculusQuestで動くようにしたものの記録用リポジトリ。

# 手順
## 準備・前置き
+ PC(windows/Mac)
+ Unity:2019.1.12f1
+ エディタ:Rider 2019.1.3(VisualStudioでもOK)
+ Unityへログインできるアカウント
+ Androidビルドできるようになっている前提

## 動作に必要なアセットの追加
Unityのアセットストアにログインして以下をマイアセットに追加
+ [UnityのVR用チュートリアルサンプルアセット](https://assetstore.unity.com/packages/essentials/tutorial-projects/vr-samples-51519)
+ [OculusQuest公式開発アセット](https://assetstore.unity.com/packages/tools/integration/oculus-integration-82022)

## Unityで新規3Dプロジェクト作成
GitHub管理するのなら先にリポジトリ準備しておくと.ignoreファイルも作れるので楽。

## Unityでのアセットダウンロード・インポート作業
新規プロジェクトを開いた状態で先程マイアセットに追加した2つのアセットをダウンロード。  
ダウンロード後、インポート。

## ビルド
1. BuildSettingsでAndroidにSwitch Platformする
1. PlayerSetting → OtherSettingsでPackageNameをこのアプリのバンドル名に設定
1. MinimumAPILevelをAPILevel23に変更
1. ビルド実行

## OculusQuestへAPKを転送
楽ちんなので、[SideQuest](https://github.com/the-expanse/SideQuest)を使用。  
ドラッグ&ドロップのみでAPK転送できる。