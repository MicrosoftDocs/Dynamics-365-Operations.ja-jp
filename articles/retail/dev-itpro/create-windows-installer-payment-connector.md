---
title: 支払コネクタ用の Windows インストーラーの作成
description: このトピックでは、支払コネクタの Windows インストーラーを作成する方法を説明します。
author: sericks007
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 141573
ms.assetid: 045bb979-989f-4f72-9eb1-6b963680b65e
ms.search.region: Global
ms.author: yabinl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 26f95754bba0823888891f5c08bfd5a54bf494a9
ms.sourcegitcommit: 27a98a7a0f1d2623f5236a88066f483def30889c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833081"
---
# <a name="create-windows-installers-for-payment-connectors"></a>支払コネクタ用の Windows インストーラーの作成

[!include [banner](../includes/banner.md)]

このトピックでは、支払コネクタの Windows インストーラーを作成する方法を説明します。 このトピックは、支払いコネクタをパッケージ化する方法を説明するために、MasterCard や Visa などの支払コネクタ プロバイダで作業する開発者を対象にしています。支払コネクタは特定顧客向けに作業する実装パートナーと共有できます。 

開発環境で支払いコネクタを実装してテストした後、生産の配置のため小売業者 IT プロフェッショナルに支払コネクタまたは付加価値再販業者 (VAR) を転送するインストーラーを作成する必要があります。 詳細については、[支払ターミナルと支払の統合](end-to-end-payment-extension.md)を参照してください。

## <a name="windows-installer"></a>Windows インストーラー
Microsoft Windows インストーラー (MSI) は、Microsoft Windows 用のアプリケーションおよび構成サービスです。 支払コネクタを配置するために必要なすべてのファイルが含まれるインストーラーを作成する必要があります。 インストーラー自体は支払コネクタを配置しません。 指定したフォルダーにコネクタ ファイルを解凍してコピーするだけです。 このトピックの次のセクションでは、そのフォルダーの内容を定義します。 インストールを続行する前に顧客がユーザー契約の受け入れを要求するように、インストーラーを構成することができます。 また、インストーラーに対して優先する形式を選択することができます。 たとえば、.exe ファイルを持つことができます。

## <a name="installer-contents"></a>インストーラーの内容
インストーラーは、次の構造で必要なファイルをインストールする必要があります。

> [!Note]
> これらのフォルダーは **...\RetailSDK\PaymentExternals** で検索することができます。

-   **PaymentExternals** – このフォルダには、最大 3 つのサブフォルダーが含まれます。
    -   **IPaymentDevice Assemblies** – このフォルダーには、IPaymentDevice インターフェイスを実装するアセンブリとその依存アセンブリが含まれています。 これらのアセンブリは、VeriFone MX925 などの決済端末デバイスと通信するために、ハードウェア ステーションおよび Retail Modern POS で使用されます。 支払のターミナル デバイスをサポートしていない場合は、このフォルダを省略できます。
    -   **IPaymentProcessor Assemblies** – このフォルダーには、IPaymentProcesor インターフェイスを実装するアセンブリとその依存アセンブリが含まれています。
    -   **支払 Web ファイル** – このフォルダには、支払受け入れページを有効にするために必要なコールバック HTML/JavaScript/CSS ファイルが含まれています。 支払い受諾ウェブ アプリケーションが Microsoft の導入ガイドに従っている場合、これらの支払いウェブ ファイルは必須ではなく、このフォルダを省略することができます。 場合によっては、支払受け入れページでは、コールバック ページをホスト アプリケーション サーバーに配置する必要があります。 その場合、コールバック ページのフォルダーを含める必要があります。
        -   **&lt;支払\_コネクタ\_名&gt;** - 異なる支払コネクタからのファイルの競合を避けるためには、支払い Web ファイルをサブフォルダ内に配置する必要があります。 サブフォルダーの名前としてコネクタ名を使用することをお勧めします。
-   **その他のユーティリティ ツール** – 決済端末装置用の構成ユーティリティなど、他のユーティリティツールがある場合は、ここに含めることができます。 支払のターミナル デバイスをサポートしていない場合は、これらのフォルダを省略できます。 ユーティリティー ツールは、支払のターミナル デバイスとのみ対話するように設計する必要があります。 ハードウェア ステーションまたは Modern POS 内のものを操作しないようにします。 ハードウェア ステーションおよび Modern POS は支払コネクタ フォルダーからファイルと共にパッケージ化されます。
-   **README.txt** – このファイルには、フォルダの内容と、含まれているユーティリティの使用方法が記載されています。 このファイルには、Cloud POS web.config および Modern POS package.appxmanifest ファイルに必要な支払いページの URL も含まれている必要があります。 支払ターミナル デバイスをサポートする場合、このファイルには、IPaymentDevice インターフェイスを実装しているアセンブリの名前も記述する必要があります。 アセンブリは、ハードウェア ステーション .config ファイルに登録されます。

次の図は、TestConnector という名前のコネクタのファイル構造を示しています。 

[![TestConnector のファイル構造](./media/paymentconnectorinstaller.png)](./media/paymentconnectorinstaller.png)



