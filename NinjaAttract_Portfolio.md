<link href="stylesheet.css" rel="stylesheet"></link>

# **「Ninja Attract」ポートフォリオ**<!-- omit in toc -->
## 河原電子ビジネス専門学校　ゲームクリエイター科2年
## 氏名：米地 真央

<br><!-- タイトル画像 -->
![title](images/title.jpg#titleImage)
<br>

***

# 目次
- [目次](#目次)
- [1.作品概要](#1作品概要)
- [2.担当ソースコード](#2担当ソースコード)
- [3.改造したエンジンコード](#3改造したエンジンコード)
- [4.ゲーム内容](#4ゲーム内容)
- [5.操作説明](#5操作説明)
- [6.困難だった点と解決方法](#6困難だった点と解決方法)
  - [6.1.hoge1](#61hoge1)
  - [6.1.hoge2](#61hoge2)
- [7.技術紹介](#7技術紹介)
  - [7.1.hoge1](#71hoge1)
  - [7.1.hoge2](#71hoge2)
- [8.ゲーム的にこだわったところ](#8ゲーム的にこだわったところ)
  - [8.1.hoge1](#81hoge1)
  - [8.2.hoge2](#82hoge2)

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

* ソースコード（cpp,h）
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
* シェーダー（fx,h）
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


<!-- 目次へのリンク_ここから -->
<section class = "goToIndexText">

[目次へ](#目次)
</section>
<!-- 目次へのリンク_ここまで -->

***

# 3.改造したエンジンコード

* ソースコード（cpp,h）
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
![gameImage](images/gameImage.jpg#normaImage)
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
![gameImage](images/Instructions.jpg#normaImage)
<br>

<!-- 目次へのリンク_ここから -->
<section class = "goToIndexText">

[目次へ](#目次)
</section>
<!-- 目次へのリンク_ここまで -->

***

# 6.困難だった点と解決方法

## 6.1.hoge1

<!-- 目次へのリンク_ここから -->
<section class = "goToIndexText">

[目次へ](#目次)
</section>
<!-- 目次へのリンク_ここまで -->


## 6.1.hoge2
&emsp;hogehoge

***

# 7.技術紹介

## 7.1.hoge1
&emsp;hogehoge

<!-- 目次へのリンク_ここから -->
<section class = "goToIndexText">

[目次へ](#目次)
</section>
<!-- 目次へのリンク_ここまで -->


## 7.1.hoge2
&emsp;hogehoge

***

# 8.ゲーム的にこだわったところ

## 8.1.hoge1
&emsp;hogehoge

<!-- 目次へのリンク_ここから -->
<section class = "goToIndexText">

[目次へ](#目次)
</section>
<!-- 目次へのリンク_ここまで -->

## 8.2.hoge2

<!-- 目次へのリンク_ここから -->
<section class = "goToIndexText">

[目次へ](#目次)
</section>
<!-- 目次へのリンク_ここまで -->