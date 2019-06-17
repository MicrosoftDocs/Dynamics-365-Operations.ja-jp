<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="uninstall-deployable-package.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>uninstall-deployable-package.d5e937.17207b63a579df40be604f62029139c86e4448bc.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>17207b63a579df40be604f62029139c86e4448bc</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\deployment\uninstall-deployable-package.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Uninstall a package</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッケージのアンインストール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to remove a deployable package from your environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、配置可能パッケージを環境から削除する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Uninstall a package</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッケージのアンインストール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Occasionally, you might have to uninstall a deployable package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">場合によっては、配置可能パッケージをアンインストールする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>For example, you might be reorganizing your source code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、ソース コードを再編成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Alternatively, you no longer require an independent software vendor (ISV) product and haven't renewed the license.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、独立系ソフトウェア ベンダー (ISV) 製品はすでに必要がなく、ライセンスを更新していません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Therefore, you must remove the package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、パッケージを削除する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Remove a model</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデルの削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>A model is a design-time concept that is part of a package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデルは、パッケージの一部であるデザイン時の概念です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>When a model isn't the only model in a module, you can just remove it from the source code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モジュール内の唯一のモデルでないモデルは、ソース コードからモデルを削除することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>No other steps are required, because when you deploy the updated module, the old module is overwritten.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">更新されたモジュールを配置するときに古いモジュールが上書きされるため、その他の手順は行う必要がありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>All overlayer models fall into this category.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのオーバーレイ モデルは、このカテゴリに分類されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>For more information, see <bpt id="p1">[</bpt>Deleting a model<ept id="p1">](../dev-tools/models.md#deleting-a-model)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>モデルの削除<ept id="p1">](../dev-tools/models.md#deleting-a-model)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Prerequisites</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前提条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>If any models reference the module that will be removed, the references must be removed from them.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">いずれかのモデルが削除されるモジュールを参照している場合、そのモジュールから参照を削除する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>For information about how to find the references that must be removed, see <bpt id="p1">[</bpt>Viewing model dependencies<ept id="p1">](../dev-tools/models.md#viewing-package-dependencies)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除する必要がある参照を検索する方法については、<bpt id="p1">[</bpt>モデルの依存関係の表示<ept id="p1">](../dev-tools/models.md#viewing-package-dependencies)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Build and deploy any modules that references were removed from.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">参照が削除されたすべてのモジュールを構築し展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>All references to and from the modules must be removed before you begin to uninstall the module.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モジュールをアンインストールする前に、モジュールへの参照およびモジュールからの参照を削除する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>To remove all a module's references, add a single class to the model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モジュールのすべての参照を削除するには、モデルに 1 つのクラスを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>This class should contain no code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このクラスにコードを含むことはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>It should contain only a reference to the application platform.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにはアプリケーション プラットフォームへの参照のみが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Uninstall a package</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッケージのアンインストール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Create a file that is named <bpt id="p1">**</bpt>ModuleToRemove.txt<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ModuleToRemove.txt<ept id="p1">**</ept> という名前のファイルを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>In the file, put the name of each module that you want to remove on a separate line.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイルには、別の行で削除する各モジュールの名前を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Make sure that you've completed the prerequisites for each module that you're removing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除する各モジュールの前提条件が完了したことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Create a valid deployable package, and put the ModuleToRemove.txt file in the <bpt id="p1">**</bpt>package<ph id="ph1">\\</ph>AOSService<ph id="ph2">\\</ph>Scripts<ept id="p1">**</ept> folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効な配置可能なパッケージを作成して、<bpt id="p1">**</bpt>package<ph id="ph1">\\</ph>AOSService<ph id="ph2">\\</ph>Scripts<ept id="p1">**</ept> フォルダに ModuleToRemove.txt ファイルを保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Install the deployable package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置可能パッケージをインストールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>For more information about how to install deployable packages, see <bpt id="p1">[</bpt>Apply updates to a cloud deployment<ept id="p1">](apply-deployable-package-system.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置可能パッケージをインストールする方法の詳細については、<bpt id="p1">[</bpt>クラウド配置に更新プログラムを適用する<ept id="p1">](apply-deployable-package-system.md)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Verify that the package was uninstalled before you complete this procedure in a production environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実稼動環境で、この手順を実行する前に、パッケージがアンインストールされたことを確認します。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>