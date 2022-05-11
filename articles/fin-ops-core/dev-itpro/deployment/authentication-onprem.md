---
title: Dynamics 365 Finance + Operations (on-premises) での認証
description: このトピックでは、認証プロセスの仕組みに関する背景情報を提供して、問題が生じる場合に解決できるようにします。
author: faix
ms.date: 11/18/2020
ms.topic: article
ms.prod: dynamics-365
ms.service: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: osfaixat
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 651f89ae12909f445ea2940d676c6215bf5c4528
ms.sourcegitcommit: 23588e66e25c05e989f3212ac519d7016820430a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2022
ms.locfileid: "8566057"
---
# <a name="authentication-in-dynamics-365-finance--operations-on-premises"></a>Dynamics 365 Finance + Operations (on-premises) での認証

[!include[banner](../includes/banner.md)]

このトピックでは、Dynamics 365 Finance + Operations (on-premises) の認証について説明します。 このトピックでは、プロセスが機能する方法に関する背景情報も提供して、認証に関する問題が発生する場合に解決できるようにします。

## <a name="the-url-for-active-directory-federation-services-ad-fs"></a>フェデレーション サービス (AD FS) の URL

認証プロセスの最初の部分は、Active Directory フェデレーションサービス (AD FS) の URL を提供することです。 この URL は次のようになります。`https://adfs.contoso.com/adfs/.well-known/openid-configuration` 

この URL は [Configure AD FS](./setup-deploy-on-premises-pu12.md#configureadfs) 内のデプロイの指示で検索できます。 デプロイ中に、URL を使用して、各 AOS インスタンスの AOS スタートアップ変数のさまざまなオプションを設定します。 これらのスタートアップ変数は、Service Fabric ディレクトリにある .XML 構成ファイルに配置されています。 このディレクトリはマシンによって異なりますが、パスは次のようになります。

C:\\ProgramData\\SF\\AOS_10\\Fabric\\work\\Applications\\AXSFType_App218\\AXSF.Package.1.0.xml

## <a name="xml-configuration-file"></a>XML 構成ファイル
AXSF.Package.Current.xml と呼ばれるファイルがあります。 このファイルは、財務と運用デプロイの AXSF.Package.1.0.xml のコピーです。 AXSF.Package.Current.xml ファイルは、現在実行中の AOS インスタンス (AxService.exe) を初期化するために使用された変数を表します。

この構成ファイル (各 AOS マシン上にある) 内には、AD FS の Lifecycle Services (LCS) のデプロイ設定から設定されているセクションのいくつかが表示されます。

```xml
<Section Name="Aad">
    <Parameter Name="AADIssuerNameFormat" Value="http://ADFS.contoso.com/{0}/services/trust" />
    <Parameter Name="AADLoginWsfedEndpointFormat" Value="https://ADFS.contoso.com/{0}/wsfed" />
    <Parameter Name="AADMetadataLocationFormat" Value="https://ADFS.contoso.com/FederationMetadata/2007-06/FederationMetadata.xml" />
    <Parameter Name="AADTenantId" Value="adfs" />
    <Parameter Name="AADValidAudience" Value="https://ax.contoso.com/" />
    <Parameter Name="ACSServiceEndpoint" Value="https://accounts.accesscontrol.windows-ppe.net/tokens/OAuth/2" />
    <Parameter Name="ACSServicePrincipal" Value="00000001-0001-0000-c000-000000000000" />
    <Parameter Name="ADFSEndpoint" Value="https://ADFS.contoso.com/adfs" />
    <Parameter Name="ADFSIdentifier" Value="http://ADFS.contoso.com/adfs/services/trust" />
    <Parameter Name="FederationMetadataLocation" Value="https://ADFS.contoso.com/FederationMetadata/2007-06/FederationMetadata.xml" />
    <Parameter Name="Realm" Value="spn:00000015-0000-0000-c000-000000000000" />
    <Parameter Name="TenantDomainGUID" Value="adfs" />
    <Parameter Name="TrustedServiceAppIds" Value="913c6de4-2a4a-4a61-a9ce-945d2b2ce2e0" />
</Section>
```
また、次のセクションも確認できます。

```xml
<Section Name="OfficeApps">
    <Parameter Name="AppInsightsKey" Value="" />
    <Parameter Name="AuthClientId" Value="d8230a86-015d-4c14-bcd6-c7fb65176b16" />
</Section>
<Section Name="OpenIDConnect">
    <Parameter Name="ClientID" Value="d8230a86-015d-4c14-bcd6-c7fb65176b16" />
    <Parameter Name="Metadata" Value="https://ADFS.contoso.com/adfs/.well-known/openid-configuration" />
</Section>
<Section Name="Provisioning">
    <Parameter Name="AdminIdentityProvider" Value="http://ADFS.contoso.com/adfs/services/trust" />
    <Parameter Name="AdminPrincipalName" Value="axserviceuser@contoso.com" />
</Section>
```

> [!NOTE]
> 上記の設定は、Microsoft 365 の互換性で構成されているデプロイを示します。 詳細については、[AD FS Microsoft 365 互換性](./onprem-adfscompatibility.md) を参照してください。

## <a name="configuration-values-used-by-the-aos"></a>AOS によって使用される構成値
AOSでは、上記の構成値が使用され、ユーザーが要求をアプリケーション URL に送信するときに、認証されていない要求をリダイレクトする場所を決定します。

1. 要求はブラウザーによりアプリケーション URL (`https://ax.contoso.com/namespaces/AXSF/`) に送信されます。
2. 要求はゲートウェイにより処理され、対話型のセッションを受け入れる AOS ノードに転送されます。
3. 要求は AOS サーバーに到達し、認証 Cookie を確認します。
4. 認証は行われないので、AOS サーバーは AD FS で認証するようにユーザーにリダイレクト要求を返します。 この時点で、AOS はアフィニティ Cookie も設定して、ユーザー セッションをその AOS にバインドします。
5. ゲートウェイは応答を受信し、ブラウザーに転送して戻します。
6. ブラウザーはリダイレクト要求を受信し、ユーザーがサインインできるように AD FS 認証ページを表示します。
7. AD FS に対して正常に認証されると、AD FS はユーザーをアプリケーション URL にリダイレクトし、認証 Cookie を提供します。
8. ゲートウェイはこの応答を受信し、アフィニティされた要求を適切な AOS ノードに転送します。
9. AOS は、提供されている認証情報を確認し、**UserInfo** テーブルに対して検証し、ユーザーが申請へのアクセスを許可されているか、およびどのアクセス許可が使用できるかを判断します。
    
AOS 構成ファイルの値が正しくない場合、通常は環境を配置するときに AD FS エンドポイントに対して提供された値が正しくないことを意味します。 最も簡単な方法は、正しい値を使用して、LCS から環境を削除して再配置することです。 構成ファイルは手動で編集できますが、安全のために再配置をします。 それ以外の場合は、各 AOS ノードで各サービス操作を実行した後に、手動で値を変更する必要があります。 構成ファイルを編集する場合は、AOS サービス (AxService.exe) を再起動して有効にする必要があります。 Service Fabric Explorer から行うことができます (**ノード** にある AOS ノードを右クリックし、**再起動** を選択し、状態が緑に変更するまで少なくとも 1 分程度待機します)。 マシンを再起動することもできます。

アプリケーション URL にアクセスするときに 500 エラーが発生するのは、AD FS に対して無効な URL がある可能性があることを示しています。 これは、AOS の起動時にその URL を使用して AD FS サーバーから情報を取得するためです。 URL が正確でないかまたはアクセスできない場合、AOS を起動することはできません。

## <a name="ad-fs"></a>AD FS
認証プロセスの 2 番目の部分は、AD FS 自体です。 AD FS サーバーで、AD FS Management を開き ((**コントロール パネル > システムとセキュリティ > 管理ツール**)、**アプリケーション グループ** に移動すると、**Microsoft Dynamics 365 for Operations オンプレミス** と呼ばれるグループが表示されます。 このグループ内では、Dynamics 365 アプリケーションの AD FS の設定が格納されます。

![AD FS 申請グループの設定。](media/ADFS.png)

AD FS は、クライアント ID および URL を使用して、アクセスの要求を受け付けるかどうかを判断します。 上記のスクリーンショットのクライアント ID は、前述の OfficeApps および OpenIDConnect セクションで指定された ID と一致していることがわかります。 クライアント ID とリダイレクト URL の両方が AOS が要求しているものと一致しない場合、AD FS は認証の要求を拒否します。 このような場合は、AD FS サーバーのイベントのログオンにエラーが見つかります。 **アプリケーションとサービス ログ > AD FS > 管理者** に、AD FS の特別なイベント ログがあります。

![AD FS のイベント ログ エラー。](media/ADFSredirectwrong.png)

AD FS 申請グループの設定に誤りがある場合、イベント ログに探していた値を説明するエラーが見つかる可能性が高いので、何が正しく設定されていないのかを判断することができます。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
