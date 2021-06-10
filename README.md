# botchies API
Yahoo様主催のOpenHackU2020(2020/8-2020/9)にて作成したAPIです．

## ハッカソンでの自分の役割
Webアプリケーション制作にて，DBと連携するAPIの制作を担当しました．

## 使用言語，環境，テクノロジー
- Go
- Goland
- Git,Github
- DBとしてGCPのCloud Firestoreを使用

## このAPIが使用されている作品の概要説明
朝早く起床することをサポートするWebアプリです。このアプリでは，起こしてほしい人に対して他の人，つまり起こす人が電話することで，起床を促します。

## API 一覧
https://github.com/ShunyaNagashige/botchies-go-backend/blob/master/swagger.yaml
| Endpoint | Method | 概要
----|----|---- 
| /show_timeline | GET | 現在時刻から20分後以内に目覚まし時刻を設定している人のデータを返す
| /reserve | POST |	設定時刻をDBに登録する
| /check_status/{peer_id} | GET | {peer_id}の人がもう目覚めたか否かを返す
| /incoming | PATCH | 特定の一人について，その人が目覚めたということをDBに登録する

## 今後の計画
- 誰でもこのAPIを利用できるようにするために，AWSにデプロイしたい(以前，このAPIをHerokuにデプロイしていました).
- 環境構築にDockerを導入したい．

- DBをMySQLにしたい．