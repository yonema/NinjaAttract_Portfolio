<link href="stylesheet.css" rel="stylesheet"></link>

# **「Ninja Attract」ポートフォリオ**<!-- omit in toc -->
## 河原電子ビジネス専門学校　ゲームクリエイター科2年
## 氏名：米地 真央

<br><!-- タイトル画像 -->
<img src = images/title.jpg class = titleImage>
<br>

***

# 目次
- [目次](#目次)
- [1.作品概要](#1作品概要)
- [2.担当ソースコード](#2担当ソースコード)
- [3.改造したエンジンコード](#3改造したエンジンコード)
- [4.ゲーム内容](#4ゲーム内容)
- [5.操作説明](#5操作説明)
- [6.技術紹介](#6技術紹介)
  - [6.1.スイングについて](#61スイングについて)
  - [6.2.インスタンシング描画](#62インスタンシング描画)
  - [6.3.FlyWeightパターン](#63flyweightパターン)
  - [6.4.D3D12のエラー、警告の回避](#64d3d12のエラー警告の回避)
- [7.ゲーム的にこだわったところ](#7ゲーム的にこだわったところ)
  - [7.1.スイングに爽快感を出すための工夫](#71スイングに爽快感を出すための工夫)
  - [7.2.IBLの影響度を書いたテクスチャの使用](#72iblの影響度を書いたテクスチャの使用)
  - [7.3.入力情報のセーブとロードによる演出](#73入力情報のセーブとロードによる演出)
  - [7.4.VRoidから自作ゲームで表示できるモデルデータへの変換](#74vroidから自作ゲームで表示できるモデルデータへの変換)

# 1.作品概要

* タイトル
  * Ninja Attract
* 学校
  * 河原電子ビジネス専門学校
* 制作人数
  * 1人
* 制作期間
  * 2021年9月～2022年2月
* ゲームジャンル
  * アクションゲーム
* プレイ人数
  * 1人
* 対応ハード
  * PC Windows10
    * Xbox 360 コントローラー
* 使用言語
  * C++
  * HLSL
* 開発環境
  * エンジン
    * 学校内製の簡易エンジン(DirectX12)
  * プログラム
    * Visual Studio 2019
  * 3Dモデル
    * 3ds MAX
    * VRoid
  * エフェクト
    * Effeckseer
  * 画像
    * Adobe Photoshop
  * バージョン管理
    * Git Hub
  * タスク管理
    * Redmine
* GitHubURL
  * [https://github.com/yonema/NinjaAttract_MyGame](https://github.com/yonema/NinjaAttract_MyGame)
* 備考
  * 就活作品用に制作
  * 第10回全国専門学校ゲームコンペティション「第10回全国専門学校ゲームコンペティション」に応募

<!-- 目次へのリンク_ここから -->
<section class = "goToIndexText">

[目次へ](#目次)
</section>
<!-- 目次へのリンク_ここまで -->

***

# 2.担当ソースコード

<details><summary>
● ソースコード（cpp,h）
</summary>

  * AABB.cpp
  * AABB.h
  * AICar.cpp
  * AICar.h
  * AICharacterBase.cpp
  * AICharacterBase.h
  * AICharacterConstData.h
  * AIConstData.h
  * AIField.cpp
  * AIField.h
  * AlphaMap.cpp
  * AlphaMap.h
  * BackGround.cpp
  * BackGround.h
  * BezierCurve.cpp
  * BezierCurve.h
  * BGM.cpp
  * BGM.h
  * BGMConstData.h
  * Bloom.cpp
  * Bloom.h
  * BuildingConstData.h
  * Buildings.cpp
  * Buildings.h
  * CascadeShadowMapMatrix.cpp
  * CascadeShadowMapMatrix.h
  * CEffectPlayer.cpp
  * CommonData.h
  * CTestMapForShadow.cpp
  * CTestMapForShadow.h
  * DebugConstData.h
  * DebugManager.cpp
  * DebugManager.h
  * DirectionalLight.cpp
  * DirectionalLight.h
  * EffectPlayer.h
  * EnemyCatchUI.cpp
  * EnemyCatchUI.h
  * Fade.cpp
  * Fade.h
  * FontRender.cpp
  * FontRender.h
  * FontRenderConstData.h
  * Game.cpp
  * Game.h
  * GameMainState.cpp
  * GameMainState.h
  * GameMainStateConstData.h
  * GameMainUI.cpp
  * GameMainUI.h
  * GameObjectNameData.h
  * GameTime.cpp
  * GameTime.h
  * GaussianBlur.cpp
  * GaussianBlur.h
  * GaussianBlurConstData.h
  * GeometryData.cpp
  * GeometryData.h
  * Goal.cpp
  * Goal.h
  * GoalConstData.h
  * Level3D.cpp
  * Level3D.h
  * LightConstData.h
  * LightData.h
  * LightManager.cpp
  * LightManager.h
  * main.cpp
  * MainMap.cpp
  * MainMap.h
  * MapChip.cpp
  * MapChip.h
  * MapConstDatah.h
  * MiniMap.cpp
  * MiniMap.h
  * MissionUI.cpp
  * MissionUI.h
  * ModelRender.cpp
  * ModelRender.h
  * ModelRenderConstData.h
  * ModelRenderData.h
  * MyEngine.cpp
  * MyEngine.h
  * NatureConstData.h
  * Noncopyable.h
  * Player.cpp
  * Player.h
  * PlayerCamera.cpp
  * PlayerCamera.h
  * PlayerCatchEnemy.cpp
  * PlayerCatchEnemy.h
  * PlayerCommandInput.cpp
  * PlayerCommandInput.h
  * PlayerConstData.h
  * PlayerInput.cpp
  * PlayerInput.h
  * PlayerModelAnimation.cpp
  * PlayerModelAnimation.h
  * PlayerMovement.cpp
  * PlayerMovement.h
  * PlayerOnEnemy.cpp
  * PlayerOnEnemy.h
  * PlayerShadowMap.cpp
  * PlayerShadowMap.h
  * PlayerStringModel.cpp
  * PlayerStringModel.h
  * PlayerSwingAction.cpp
  * PlayerSwingAction.h
  * PlayerWalkAndRun.cpp
  * PlayerWalkAndRun.h
  * PlayerWallRun.cpp
  * PlayerWallRun.h
  * PointLight.cpp
  * PointLight
  * PostEffect.cpp
  * PostEffect.h
  * PostEffectConstData.h
  * PriorityData.h
  * ProtoMap.cpp
  * ProtoMap.h
  * Render.cpp
  * Render.h
  * RenderingEngine.cpp
  * RenderingEngine.h
  * RenderingEngineConstData.h
  * SavedPlayerInputData.cpp
  * SavedPlayerInputData.h
  * SavedPlayerInputDataConstData.h
  * SceneGeometryData.cpp
  * SceneGeometryData.h
  * ShadowConstDatah.h
  * ShadowMapRender.cpp
  * ShadowMapRender.h
  * SkyCube.cpp
  * SkyCube.h
  * SoundCue.cpp
  * SoundCue.h
  * SpotLight.cpp
  * SpotLight.h
  * SpringCamera.cpp
  * SpringCamera.h
  * SpriteRender.cpp
  * SpriteRender.h
  * SpriteRenderConstData.h
  * StopWatch.h
  * StringActionTargetManager.cpp
  * StringActionTargetManager.h
  * SwingTarget.cpp
  * SwingTarget.h
  * TestMap.cpp
  * TestMap.h
  * TestMapForLevel3D.cpp
  * TestMapForLevel3D.h
  * TestMapForPlayerMove.cpp
  * TestMapForPlayerMove.h
  * TestMapForSpotLight.cpp
  * TestMapForSpotLight.h
  * TextPanelRender.cpp
  * TextPanelRender.h
  * TitleMap.cpp
  * TitleMap.h
  * TklFile.cpp
  * TklFile.h
  * TResourceBank.h
  * UIConstData.h
  * Util.h
  * VectorRender.cpp
  * VectorRender.h
</details>

<details><summary>
● シェーダー（fx,h）
</summary>

  * bloom.fx
  * DeferredLighting.fx
  * DrawShadowMap.fx
  * gaussianBlur.fx
  * miniMap.fx
  * ModelVSCommon.h
  * PBRLighting.h
  * PointAndSpotLightFunc.h
  * RenderToGBufferFor3DModel.fx
  * SkyCubeMap.fx
  * TranslucentModel.fx
</details>

<!-- 目次へのリンク_ここから -->
<section class = "goToIndexText">

[目次へ](#目次)
</section>
<!-- 目次へのリンク_ここまで -->

***

# 3.改造したエンジンコード

<details><summary>
● ソースコード（cpp,h）
</summary>

  * stdafx.h
    * CommonData.hのインクルードの追加（6行目）
  * EffectEngine.cpp
    * DXGI_FORMATの変更（16行目）
  * CaslFile.cpp
    * 読み込んだデータと受け取る変数がずれているバグがあったため修正（56行目）
  * Level2D.cpp
    * レイヤー番号を受け取るように変更（43行目）
  * Level2D.h
    * レイヤー番号用のデータメンバを追加（20行目）
  * Physics.cpp
    * コールバック用の構造体の追加（24行目～40行目）
  * Physics.h
    * 当たり判定用の関数の追加（126行目～135行目）
  * Animation.h
    * 配列の-1番目の要素にアクセスするバグがあったため修正（137行目）
    * アニメーションの残り時間（比率）を得る関数を追加（207行目～211行目）
  * AnimationPlayController.cpp
    * アニメーションの残り時間（比率）の計算処理を追加（148行目）
  * AnimationPlayController.h
    * アニメーションの残り時間（比率）用のデータメンバを追加（143行目）
  * FontEngine.cpp
    * DXGI_FORMATの変更（30行目）
  * GraphicsEngine.cpp
    * 使用するGPUの種類を決める処理で、メモリリークが発生していたため修正（232行目～305行目）
  * GamePad.cpp
    * ゲームパッドのRT（RB2）とLT（LB2）のトリガー判定がプレス判定と同じになっているバグがあったので修正（109行目～115行目）
  * Material.cpp
    * 固定だったカリング設定を、自由に設定できるように変更（288行目）
    * 同じテクスチャが使用されている時、リソースを使いまわすように変更（15行目～219行目）
    * 同じシェーダーが使用されている時、リソースを使いまわすように変更（347行目～393行目）
  * Material.h
    * 一部データメンバをポインタに変更（124行目～126行目）
  * MeshParts.cpp
    * 定数バッファを配列で指定できるように変更（54行目～60行目、103行目～108行目、229行目～234行目）
    * シェーダーリソースビューを配列で指定できるように変更（94行目～99行目）
  * MeshParts.h
    * 共通で使われる定数バッファの中身にパラメータを追加（138行目～139行目）
    * 共通定数バッファのパラメータの増設に伴い、描画関数の引数も増設（63行目～74行目）
    * 初期化用関数の引数の変更（45行目～56行目）
  * Model.h
    * 初期化用データのパラメータを増設（30行目～49行目）
    * 一部データメンバをポインタに変更（121行目）
  * NullTextureMaps.cpp
    * ヌルテクスチャのファイルパスを保持する処理を追加（30行目～ 54行目）
  * NullTextureMaps.h
    * ヌルテクスチャのファイルパスを保持するデータメンバの追加と、そのデータメンバのゲッター関数（118行目～161行目）
  * Sprite.cpp
    * 固定だったスプライトのアドレッシングモードを、指定できるように変更（225行目～227行目）
    * 定数バッファを配列で指定できるように変更（94行目～99行目、197行目～208行目、296行目～302行目）
    * 複数のスプライトのカラーバッファーフォーマットを指定できるように変更（178行目～184行目）
  * Sprite.h
    * スプライトに設定できる最大テクスチャ数の増設（11行目）
    * 初期化用データのパラメータの増設（37行目～59行目）
    * スプライトのパラメータを変更、取得をするメンバ関数の追加（163行目～217行目）
    * 一部のデータメンバをポインタに変更（221行目～223行目）
  * Texture.cpp
    * キューブマップ用のテクスチャにも対応するように変更（78行目～88行目、109行目～118行目）
  * TkmFile.cpp
    * 同じddsファイルが使用される時、リソースを使いまわすように変更（240行目～265行目）
  * TkmFile.h
    * マテリアルに、テクスチャのファイルパスを保持し続けるように変更（41行目～45行目）
</details>

<!-- 目次へのリンク_ここから -->
<section class = "goToIndexText">

[目次へ](#目次)
</section>
<!-- 目次へのリンク_ここまで -->

***

# 4.ゲーム内容
&emsp;街中を自由にスイングで飛び回れる、3Dスイングアクションゲーム。<br>
危険走行をする暴走車を、スイングで追いかけて捕まえろ！

<br><!-- ゲームのイメージ画像 -->
<img src = images/gameImage.jpg class = normalImage>
<br>


<!-- 目次へのリンク_ここから -->
<section class = "goToIndexText">

[目次へ](#目次)
</section>
<!-- 目次へのリンク_ここまで -->

***

# 5.操作説明

* Aボタン：ジャンプ
* Yボタン：（車の近くで）車の上に乗る
* RT（R2ボタン）：（地上で）ダッシュ、（空中で）スイング
* 左スティック：移動
* 右スティック：カメラ回転
* 右スティック→押し込み：敵探知
* STARTボタン：ミッション確認

<br><!-- 操作説明の画像 -->
<img src = images/Instructions.jpg class = normalImage>
<br>

<!-- 目次へのリンク_ここから -->
<section class = "goToIndexText">

[目次へ](#目次)
</section>
<!-- 目次へのリンク_ここまで -->

***

# 6.技術紹介

## 6.1.スイングについて
&emsp;このゲームのスイングアクションは、プレイヤーが鎖を射出し、鎖の先端がビルに引っ付き、そこを中心に振り子のような動きのスイングアクションで移動する。このスイングアクションは以下のような流れで実行している。

1. ビルの鎖の射出先の候補地（以降**スイングターゲット**）の位置を計算する。
2. 鎖が射出するスイングターゲットを探す。
3. スイングターゲットに向かって、鎖を射出する。鎖がスイングターゲットまで届いたらスイング開始。
4. 進む方向の上下の角度を求める。
5. 進むスピードを求める。
6. スイング中の左右の方向転換を計算する。
7. プレイヤーに移動速度を加算する。

&emsp;それぞれの手順を詳しく見ていく。

1. **ビルのスイングターゲットの位置を計算する**
   1. ビルのモデルデータをもとにAABBを作成する。まずは、モデルの頂点データを1つずつ調べ、最大座標と最小座標を求める。
   2. ( 最大座標 - 最小座標 ) × 0.5f を計算してAABBの半分のサイズを求める。
   3. ( 最大座標 + 最小座標 ) × 0.5f を計算してAABBのセンターポジションを求める。
   4. AABBのセンターポジションと半分のサイズから、AABBの8頂点を求める。
   5. 4.で求めたAABBは、まだ、オブジェクト座標系のAABBのため、ビルのワールド行列をAABBに乗算して、ワールド座標系のAABBを求める。
   6. このAABBの側面にスイングターゲットを等間隔で配置する。この時、一定以下の高さはスイング出来ないので、除外する。
    
      <br><!-- スイングの画像 -->
      <img src = images/swing1.jpg class = normalImage>
      <br>

1. **鎖が射出するスイングターゲットを探す**
   1. まず、スイングで進む方向を決める。移動入力があったらその方向に、無かったらカメラの前方向がスイングで進む方向になる。
   2. プレイヤーの座標から、スイングで進む方向に一定距離先の座標を基点に、有効範囲内にあって一番近いスイングターゲットを探し出す。この時、進む方向ベクトルと、プレイヤー座標からスイングターゲットへの方向ベクトルの内積が負になるスイングターゲットは候補から除外する。つまり、進む方向と逆方向のスイングターゲットは選ばないようにする。

      ▽上から見たスイングターゲットを探す処理
      <br><!-- スイングの画像 -->
      <img src = images/swing2.jpg class = normalImage>
      <br>

2. **スイングターゲットに向かって、鎖を射出する。鎖がスイングターゲットまで届いたらスイング開始**
   1. 選んだスイングターゲットに向かって鎖を射出する。
   2. プレイヤーの座標からスイングターゲットの座標へ線形補完を行い、補間率を挙げていくことによって鎖を伸ばしていく。そのため、プレイヤーとスイングターゲットの間の距離に関係なく一定の時間で伸びきる。
   3. 鎖のモデルを拡大させてスイングターゲットまで伸ばしてしまうと、ゴムのように伸びた鎖のモデルになってしまう。それを防ぐために、鎖のモデルを2つ用意する。1つ目のモデルは手元から伸ばしていき、等倍まで伸びたら先端から2つ目の鎖のモデルの伸ばし始める。2つ目のモデルはそのままスイングターゲットまで伸ばす。こうすることで、カメラに映っている手元の鎖のモデルは正常な倍率で表示さる。2つ目のモデルはあまりカメラに映らないため、伸びていても目立たない。
   4. 鎖がスイングターゲットまで伸びきったら、スイングを開始する。

      <br><!-- スイングの画像 -->
      <img src = images/swing3.jpg class = normalImage>
      <br>

3. **進む方向の上下の角度を求める**
   1. スイング中の動きを計算していく。振り子のような動きで前の進むため、上下の動きがある。まずはその上下の角度を求める。
   2. 最初にプレイヤーの座標からスイングターゲットまでのベクトルを求めて、そのベクトルのY成分を消す。これで**XZ平面でのプレイヤーからスイングターゲットへのベクトル**が求まる。
   3. 次に、「鎖が射出するスイングターゲットを探す」ときに求めたスイングで進む方向、これを**XZ平面での前方向ベクトル**とする。

      <br><!-- スイングの画像 -->
      <img src = images/swing4.jpg class = normalImage>
      <br>

   4. **XZ平面での前方向ベクトル**に内積を使って**XZ平面でのプレイヤーからスイングターゲットへのベクトル**を射影する。

      <br><!-- スイングの画像 -->
      <img src = images/swing5.jpg class = normalImage>
      <br>
  
   5. **XZ平面での前方向ベクトル**に射影して求めた長さを乗算して、**XZ平面でのプレイヤーからスイングターゲットへのベクトル**を、**XZ平面での前方向ベクトル**に射影したベクトルが求まる。

   6. プレイヤーの座標に 5. で求めたベクトルを加算すると**XZ平面でのスイングターゲットをプレイヤーの前方向に直交するように移動させた座標**が求まる。

      <br><!-- スイングの画像 -->
      <img src = images/swing6.jpg class = normalImage>
      <br>

   7. 6.の座標のY座標をスイングターゲットのY座標と同じにする。これでスイングターゲットをプレイヤーの前方向までずらした座標が求まる。この座標を振り子の支点に見立てて移動させる。プレイヤーの前方向にずらしたため、真っ直ぐ前に振り子運動をする。本来ならそのままのスイングターゲットの座標を支点とするのが正しいが、プレイヤーの操作性やスイングの爽快感を出すために、プレイヤーの前方向までずらしている。

      <br><!-- スイングの画像 -->
      <img src = images/swing7.jpg class = normalImage>
      <br>

   8. **前方向にずらしたスイングターゲットからプレイヤーへの方向ベクトル**を求め、**XZ平面での前方向ベクトル**と内積をとる。
   9. 内積が負なら、プレイヤーはスイングターゲットより手前におり、正ならスイングターゲットより奥にいる。手前の時と奥の時で処理を変える。

      <br><!-- スイングの画像 -->
      <img src = images/swing9.jpg class = normalImage>
      <br>

   10. 手前にいるときの処理は、**XZ平面での前方向ベクトル**を下に回転させる。下向きに回転させるために回転軸を求める。**上方向のベクトル**と**XZ平面での前方向ベクトル**の外積を求め、上下の回転に必要な**横方向ベクトル**が求まる。 
      <br><!-- スイングの画像 -->
      <img src = images/swing9.jpg class = normalImage>
      <br>
      
   11. 次に回転量を求める。回転量は8.で求めた内積の数値に応じて決める。8.の内積は-1.0f～0.0fの値をとり、-1.0fの時は回転量0度、-0.5fのときは回転量90度、0.0fの時は回転量0度になるような二次関数の式で変化させる。これで最初は真っ直ぐ進み、だんだん下方向へ進むようになって、また真っ直ぐに戻っていくとう変化になる。
   12. 式は、y = -4(X + 0.5)^2 + 1.0となり、xに内積を入れる。するとyの値が0.0->1.0->0.0と変化する。そして回転量90度にyの値をかける。
   13. **XZ平面での前方向ベクトル**を10.で求めた**横方向ベクトル**を軸中心に、12.で求めた回転量だけ回転させ、上下の角度を決める。
      <br><!-- スイングの画像 -->
      <img src = images/swing10.jpg class = normalImage>
      <br>

   14. 9.の時に内積が正のとき処理は**前方向にずらしたスイングターゲットからプレイヤーへの方向ベクトル**を**横方向ベクトル**で90度回転させたベクトルの方向に進む。
      <br><!-- スイングの画像 -->
      <img src = images/swing11.jpg class = normalImage>
      <br>

4. **進むスピードを求める**
   1. スイングのスピードは、任意の位置での振り子の速度の公式を使用。<br>


 $$
 g = 重力加速度\\
 l = 振り子の長さ\\
 v任 = 任意の場所での振り子の速度\\
 \cos\theta任 = 任意の場所の角度\\
 \cos\theta上 = 一番上の時の角度\\
 V任 = \sqrt{2lg}(\cos\theta任 - \cos\theta上)
 $$
   
   2. cosΘ任には、**前方向にずらしたスイングターゲットからプレイヤーへの方向ベクトル**と**下方向ベクトル**の内積が入る。
   3. cosΘ上には、一番上の時の角度は90度のため0.0が入る。
   4. gに重力加速度、lに振り子の長さ（鎖の長さ）を入れる。
   5. ここで、**前方向にずらしたスイングターゲットからプレイヤーへの方向ベクトル**と**XZ平面での前方向ベクトル**と内積をとって、プレイヤーがスイングターゲットより手前側にいた場合と奥側にいた場合で処理をわける。
   6. 手前側にいた場合、任意の位置での振り子の速度の公式の、角度による減速を行わない。そのため√2lgのみ行う。
   7. 奥側にいた場合、任意の位置での振り子の速度の公式の、すべての計算を行う。上に行けば行くほど減速していく。

5. スイング中の左右の方向転換を計算する
   1. 左右の移動入力があれば、カメラの左右方向に力を加える。
   2. 力が加わって急に方向が変わり過ぎないように、現在の左右への方向転換量と目標の方向転換量を線形補完を行って緩やかに変化するようにしている。

6. プレイヤーに移動速度を加算する
   1. これまで計算したスイングの移動ベクトルをプレイヤーに加算する。
   2. プレイヤーの移動速度が速くなり過ぎないように、速度制限を付ける。

<!-- 目次へのリンク_ここから -->
<section class = "goToIndexText">

[目次へ](#目次)
</section>
<!-- 目次へのリンク_ここまで -->


<!-- ## 6.2.カスケードシャドウ
&emsp;hogehoge -->

<!-- 目次へのリンク_ここから -->
<!-- <section class = "goToIndexText">

[目次へ](#目次)
</section> -->
<!-- 目次へのリンク_ここまで -->

<!-- ## 6.3.EVSM
&emsp;hogehoge -->

<!-- 目次へのリンク_ここから -->
<!-- <section class = "goToIndexText">

[目次へ](#目次)
</section> -->
<!-- 目次へのリンク_ここまで -->

<!-- ## 6.4.PBR
&emsp;hogehoge -->

<!-- 目次へのリンク_ここから -->
<!-- <section class = "goToIndexText">

[目次へ](#目次)
</section> -->
<!-- 目次へのリンク_ここまで -->

## 6.2.インスタンシング描画
&emsp;インスタンシング描画とは、同じモデルを複数表示するときに、本来表示する数だけドローコールを呼ばなければいけないところを、1回のドローコールだけで実現できる技術である。ドローコールを減らすことでCPUのパフォーマンスを向上できる。

<section class = "box27">
<span class = "box-title">POINT</span>
インスタンシング描画はGPUのパフォーマンスを向上してくれるのではなく、CPUのパフォーマンスを向上してくれるものである。<br>
ドローコールを削減しても、結局GPUで計算する頂点数やライティングの量は変わらないためである。
</section>

<br><!-- インスタンシング描画の説明の画像 -->
<img src = images/instancing1.jpg class = normalImage>
<br>

&emsp;インスタンシング描画の手順は以下の通りである。

1. （ここからCPU側の処理）ワールド行列の配列の用意し、ワールド行列の配列をGPUのシェーダーリソースビューに渡す。この時、配列のはずは動的のため、定数バッファではなくストラクチャードバッファを使用する。
2. ワールド行列の配列を更新する。
3. ワールド配列の配列を使用し、ストラクチャードバッファを更新する
4. 表示するモデルの数をインスタンス数として指定して、モデルのドローコールを呼ぶ。
5. （ここからGPU側の処理）GPU側で送られてきたワールド行列の配列をtレジスタを介して変数に保持。
6. 頂点シェーダーに、HLSLが用意してあるSV_InstanceIDセマンティクスを指定した引数を追加し、現在処理しているインスタンス番号が分かるようにする。
7. ワールド行列の配列からインスタンス番号で適切なワールド行列を取得し、座標変換を行う。

<!-- 目次へのリンク_ここから -->
<section class = "goToIndexText">

[目次へ](#目次)
</section>
<!-- 目次へのリンク_ここまで -->

<!-- ## 6.6.フラスタムカリング
&emsp;hogehoge -->

<!-- 目次へのリンク_ここから -->
<!-- <section class = "goToIndexText">

[目次へ](#目次)
</section> -->
<!-- 目次へのリンク_ここまで -->

<!-- ## 6.7.LOD
&emsp;hogehoge -->

<!-- 目次へのリンク_ここから -->
<!-- <section class = "goToIndexText">

[目次へ](#目次)
</section> -->
<!-- 目次へのリンク_ここまで -->

## 6.3.FlyWeightパターン

&emsp;大量にあるビルや街路樹は、同じモデルやテクスチャを使用しているものが沢山ある。街路樹は全て同じモデルが使用されている。ビルのモデルは29あるが、違うモデルでも同じテクスチャを使用しているところが何か所もある。このような場合では、FlyWeightパターンを使用すれば、大幅にメモリ使用量を節約することができる。

▽同じモデルを使用しているの街路樹
<br><!-- リソースバンクの説明の画像 -->
<img src = images/ResourceBank1.jpg class = normalImage>
<br>

▽同じテクスチャを使用しているビル
<br><!-- リソースバンクの説明の画像 -->
<img src = images/ResourceBank2.jpg class = normalImage>
<br>

普通に読み込むと、同じモデルやテクスチャを使用していても、使用する分だけオブジェクトの生成を行うことになる。その時の使用メモリ量は、オブジェクつに   必要のメモリ量×オブジェクトの数になってしまう。<br>
だが、FlyWightパターンを使用した場合、最初に生成するときにリソースバンクにリソースを登録する。2回目以降は、リソースバンクからリソースの参照をため   新たに生成する必要がなくなる。そのため、使用メモリ量は、オブジェクト1つに必要なメモリ量だけになる。<br>
これにより、当初は20GB以上のメモリを使用していたステージが、約5GBのメモリ使用量で生成することが出来た。

▽FlyWightパターン無しの場合
<br><!-- リソースバンクの説明の画 -->
<img src = images/ResourceBank3.jpg class = normalImage>
<br>

▽FlyWightパターン有りの場合
<br><!-- リソースバンクの説明の画 -->
<img src = images/ResourceBank4.jpg class = normalImage>
<br>

<!-- 目次へのリンク_ここから -->
<section class = "goToIndexText">

[目次へ](#目次)
</section>
<!-- 目次へのリンク_ここまで -->

<!-- ## 6.9.ベジェ曲線
&emsp;hogehoge -->

<!-- 目次へのリンク_ここから -->
<!-- <section class = "goToIndexText">

[目次へ](#目次)
</section> -->
<!-- 目次へのリンク_ここまで -->

## 6.4.D3D12のエラー、警告の回避
&emsp;VisualStudioの出力ウィンドウに表示されるD3D12のエラー、警告を全て回避した。このエラーが表示されていても、ゲームは動いているため、今まで気にしていなかったが、今回はこれらのエラーを全て除去することが出来た。

<br><!-- D3D12の警告、エラーの画像 -->
<img src = images/d3d12Error1.jpg class = normalImage>
<br>

遭遇したエラーは主に次の三種類である。

1. STATE_CREATION WARNING #0: UNKNOWN
2. EXECUTION ERROR #613: RENDER_TARGET_FORMAT_MISMATCH_PIPELINE_STATE
3. EXECUTION ERROR #538: INVALID_SUBRESOURCE_STATE

これらのエラーの種類、発生した場所、解決方向は以下の通りである。

1. **STATE_CREATION WARNING #0: UNKNOWN**
   1. 警告の種類
      * この警告はメモリリークの警告である。生成したオブジェクトを最後まで解放していないことが原因で出る警告だ。
   2. 発生した場所
      * この警告は、ゲームを終了した時に発生。
      * 出力ウィンドウには、次のように表示された。
```
D3D12 WARNING: 	Live Object at 0x000001CCE55079B0, Refcount: 0. [ STATE_CREATION WARNING #0: UNKNOWN]
```
   3. 解決方法
      * 全体検索で、オブジェクトを生成している場所を探し、きちんと破棄しているか確認し、解放するようにする。
      * コードの一部をコメントアウトしてみて、症状が改善したか調べ、原因を特定し、解放するようにする。
      * newでオブジェクトを生成するのではなく、スマートポインタのstd::unique_ptrを使用する。これにより、解放し忘れを防ぐ。

2. **EXECUTION ERROR #613: RENDER_TARGET_FORMAT_MISMATCH_PIPELINE_STATE**
   1. エラーの種類
      * このエラーは、レンダリングターゲットを生成するときに指定したカラーフォーマットと、そのレンダリングターゲットに描画するオブジェクトのカラーフォーマットが違っている、というエラーだ。
   2. 発生した場所
      * G-Bufferにモデルを描画するときに発生。
      * エフェクト、スプライトを描画するときに発生。
      * 出力ウィンドウには、次のように表示された。
```
D3D12 ERROR: ID3D12CommandList::DrawIndexedInstanced: The render target format in slot 0 does not match that specified by the current pipeline state. (pipeline state = R16G16B16A16_FLOAT, RTV ID3D12Resource* = 0x000001CC784F0360:'Unnamed ID3D12Resource Object') [ EXECUTION ERROR #613: RENDER_TARGET_FORMAT_MISMATCH_PIPELINE_STATE]

```
   3. 解決方法
      * G-Bufferにマルチレンダリングターゲットを利用してモデルを描画するとき、モデルに1つしかカラーフォーマットし指定していなかった。モデルに複数のカラーフォーマットを指定できるようにし、G-Bufferのカラーフォーマットと合わせることで解決した。
      * エフェクトとスプライトは学校内製の簡易エンジンで最初から表示されていたため、カラーフォーマットを合わせることを見落としていた。指定している場所を調べ、修正した。

3. **EXECUTION ERROR #538: INVALID_SUBRESOURCE_STATE**
   1. エラーの種類
      * これはレンダリングターゲットのサブリソースが不正、というエラーだ。
   2. 発生した場所
      * ポストエフェクトをかけたあと、スプライトを描画使用としたときに発生。
      * 出力ウィンドウには、次のように表示された。
```
D3D12 ERROR: ID3D12CommandList::DrawIndexedInstanced: Resource state (0x0: D3D12_RESOURCE_STATE_[COMMON|PRESENT]) of resource (0x000001CC784F0360:'Unnamed ID3D12Resource Object') (subresource: 0) is invalid for use as a render target.  Expected State Bits (all): 0x4: D3D12_RESOURCE_STATE_RENDER_TARGET, Actual State: 0x0: D3D12_RESOURCE_STATE_[COMMON|PRESENT], Missing State: 0x4: D3D12_RESOURCE_STATE_RENDER_TARGET. [ EXECUTION ERROR #538: INVALID_SUBRESOURCE_STATE]
```
   3. 解決方法
      * レンダリングの処理を一部ずつコメントアウトしていき、改善していないか調べて、原因がポストエフェクト後のスプライト描画する時だと判明。
      * ポストエフェクトを実行した後スプライトを描画する際、レンダリングターゲットが使用可能になるまで待つ処理を入れ忘れていたため、修正。


<!-- 目次へのリンク_ここから -->
<section class = "goToIndexText">

[目次へ](#目次)
</section>
<!-- 目次へのリンク_ここまで -->

***

# 7.ゲーム的にこだわったところ

## 7.1.スイングに爽快感を出すための工夫
&emsp;スイングの爽快感を出すために、スイングで速く移動できるようにしたが、速すぎてとても操作が難しくなってしまった。そのため、速度はそのままで速く動いているように見せるために、バネカメラの減衰率をスイング中に動的に調整した。スイング中は減衰率を上げて、カメラがより遅れてくるようにする。これによりプレイヤーが加速して動いたかのように見える。

<!-- 目次へのリンク_ここから -->
<section class = "goToIndexText">

[目次へ](#目次)
</section>
<!-- 目次へのリンク_ここまで -->

## 7.2.IBLの影響度を書いたテクスチャの使用
&emsp;IBLを利用して、モデルに空を反射させている。この時IBLの影響度をモデルに貼られているテクスチャから決めている。これにより、ビルに空を反射させるとき、壁はそこそこ反射、窓にはくっきりと反射させることができる。

▽IBLの影響度の設定のない空の反射
<br><!-- IBLの影響度の画像 -->
<img src = images/iblLevel1.jpg class = normalImage>
<br>

▽IBLの影響度の設定がある空の反射
<br><!-- IBLの影響度の画像 -->
<img src = images/iblLevel2.jpg class = normalImage>
<br>

▽ビルの窓に貼っているテクスチャ。rgbaの内、gの値がIBLの影響度
<br><!-- IBLの影響度の画像 -->
<img src = images/iblLevel3.jpg class = miniImage>
<br>

<!-- 目次へのリンク_ここから -->
<section class = "goToIndexText">

[目次へ](#目次)
</section>
<!-- 目次へのリンク_ここまで -->

## 7.3.入力情報のセーブとロードによる演出
&emsp;タイトルシーンでプレイヤーがスイングで遠くに飛んでいく演出がある。これは、入力情報のセーブとロードに依って実現した。入力情報は、コントローラーの入力情報とそのフレームのデルタタイムを毎フレーム収集している。

1. タイトル画面で、自分でプレイヤーを動かす。その時の入力情報を保存する。
2. 保存した入力情報を読み込んで、プレイヤーに渡して再生する。

<!-- 目次へのリンク_ここから -->
<section class = "goToIndexText">

[目次へ](#目次)
</section>
<!-- 目次へのリンク_ここまで -->

<!-- ## 7.4.ミニマップや敵探知のUI実装 -->

<!-- 目次へのリンク_ここから -->
<!-- <section class = "goToIndexText">

[目次へ](#目次)
</section> -->
<!-- 目次へのリンク_ここまで -->

<!-- ## 7.5.QTEの演出 -->

<!-- 目次へのリンク_ここから -->
<!-- <section class = "goToIndexText">

[目次へ](#目次)
</section> -->
<!-- 目次へのリンク_ここまで -->

## 7.4.VRoidから自作ゲームで表示できるモデルデータへの変換
&emsp;このゲームのプレイヤーのモデルには、VRoidというキャラクターモデリングソフトを使用して自作したモデルを使用している。だが、このVRoidはモデルのエクスポートがvrmファイルという独自の形式しかサポートしていない。このゲームではtkmという学内エンジン用のフォーマットのモデルを使用している。このモデルに変換するために3ds Maxという3DCGソフトに取り込む必要がある。

1. UniVRMパッケージを使いVroidからUnityへ（テクスチャのカラーが変）
2. Windows10標準搭載の3D Builderを使いobjに変換（UVが変）

<!-- 目次へのリンク_ここから -->
<section class = "goToIndexText">

[目次へ](#目次)
</section>
<!-- 目次へのリンク_ここまで -->

<!-- # 9.今後の課題

## 9.1.スイング中のカーブがしずらい

## 9.2.スイングをもっと気持ちよ

## 9.3.額あて、マフラーなどを付けて、風になびかせる

## 9.4.カスケードシャドウの切り替わりが目立つ

## 9.5.プレイヤー用の影のソフトシャドウ

## 9.6.街が単調

## 9.7.スイング以外の移動アクションを増やす

## 9.8.ドローンなどの空中の敵 -->

<!-- 目次へのリンク_ここから -->
<!-- <section class = "goToIndexText">

[目次へ](#目次)
</section> -->
<!-- 目次へのリンク_ここまで -->





