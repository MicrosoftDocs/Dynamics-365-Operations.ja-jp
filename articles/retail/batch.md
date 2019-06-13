<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="batch.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-d915bc8" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>batch.e70006.4456fc3d5bc4547fa8211642b11ca6df455fa187.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>4456fc3d5bc4547fa8211642b11ca6df455fa187</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>aec1dcd44274e9b8d0770836598fde5533b7b569</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>06/03/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\batch.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Improved handling of batch-tracked items</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">バッチ追跡品目の処理の改善</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes the improvements that have been made to the handling of batches for batch-tracked items during the Retail statement posting process.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このトピックでは、小売明細書転記プロセス時のバッチ追跡品目のバッチの処理に対して行われた改善について説明します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Improved handling of batch-tracked items</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">バッチ追跡品目の処理の改善</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>In Microsoft Dynamics 365 for Retail Point of Sale (POS), batch numbers can't be captured for batch-tracked items at the time of sale.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Microsoft Dynamics 365 for Retail 販売時点管理 (POS) では、バッチ追跡品目のバッチ番号を販売時に取得することはできません。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>However, for specific configurations, when sales are posted in the headquarters through customer orders or statement posting, the Microsoft Dynamics system expects that valid batch numbers for batch-tracked items exist, and that they will be used during the invoicing process.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ただし、特定の構成では、顧客の注文または明細書の転記を通じて販売が本社に転記されるとき、Microsoft Dynamics システムは、バッチ追跡品目に対して有効なバッチ番号が存在することと、請求プロセスで有効なバッチ番号が使用されることを想定しています。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>If valid batch numbers are available for products, the customer order invoicing process and the sales order invoicing process from statement posting use them.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">製品に対して有効なバッチ番号が存在する場合は、顧客注文の請求プロセスと、明細書の転記からの販売注文請求プロセスでそのバッチ番号が使用されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Otherwise, the customer order invoicing process can't post, and the POS user receives an error message.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">それ以外の場合、顧客注文請求プロセスは転記できず、POS ユーザーにはエラー メッセージが表示されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Statement posting then goes into an error state.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">その結果、明細書を転記しようとするとエラー状態になります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>This error state occurs even when negative inventory has been turned on for the products.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このエラー状態は、製品のマイナス在庫が有効になっていても発生します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Improvements that have been made in Microsoft Dynamics for Retail version 10.0.4 and later help guarantee that, when negative inventory is turned on for batch-tracked items, customer order invoicing and sales order invoicing through statement posting aren't blocked for those items if the inventory is 0 (zero) or a batch number isn't available.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Microsoft Dynamics for Retail バージョン 10.0.4 以降で行われた改善では、バッチ追跡品目に対してマイナス在庫が有効になっているとき、在庫が 0 (ゼロ) であるか、またはバッチ番号が使用できない場合、明細書の転記を通じた顧客注文の請求と販売注文の請求がブロックされないことが保証されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The new functionality uses a default batch ID for the sales lines when batch numbers aren't available.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">この新しい機能では、バッチ番号が使用できないとき、販売明細行の既定のバッチ ID が使用されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>To define the default batch ID that is used for customer orders, on the <bpt id="p1">**</bpt>Retail parameters<ept id="p1">**</ept> page, on the <bpt id="p2">**</bpt>Customer orders<ept id="p2">**</ept> tab, on the <bpt id="p3">**</bpt>Order<ept id="p3">**</ept> FastTab, set the <bpt id="p4">**</bpt>Default batch id<ept id="p4">**</ept> field.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">顧客注文に使用される既定のバッチ ID を定義するには、<bpt id="p1">**</bpt>小売パラメーター<ept id="p1">**</ept> ページの <bpt id="p2">**</bpt>顧客注文<ept id="p2">**</ept> タブの <bpt id="p3">**</bpt>注文<ept id="p3">**</ept> クイック タブで、<bpt id="p4">**</bpt>既定のバッチ ID<ept id="p4">**</ept> フィールドを設定します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>To define the default batch ID that is used for sales order invoicing through statement posting, on the <bpt id="p1">**</bpt>Retail parameters<ept id="p1">**</ept> page, on the <bpt id="p2">**</bpt>Posting<ept id="p2">**</ept> tab, on the <bpt id="p3">**</bpt>Inventory update<ept id="p3">**</ept> FastTab, set the <bpt id="p4">**</bpt>Default batch id<ept id="p4">**</ept> field.</source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match">明細書の転記を通じた販売注文の請求に使用される既定のバッチ ID を定義するには、<bpt id="p1">**</bpt>小売パラメーター<ept id="p1">**</ept> ページの <bpt id="p2">**</bpt>転記<ept id="p2">**</ept> タブの <bpt id="p3">**</bpt>在庫更新<ept id="p3">**</ept> クイック タブで、<bpt id="p4">**</bpt>既定のバッチ ID<ept id="p4">**</ept> フィールドを設定します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>This functionality is available only when advanced warehousing is turned on for the specific store warehouse and items.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">この機能は、特定の店舗倉庫および品目に対して高度な倉庫管理が有効になっている場合にのみ使用できます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>In a later release, the functionality will also be supported for scenarios where advanced warehouse management isn't used.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">後のリリースでは、この機能は、高度な倉庫管理が使用されていない場合にもサポートされます。</target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>