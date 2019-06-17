<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="implement-multiple-projects-aad-tenant.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>implement-multiple-projects-aad-tenant.871e6c.b8c6dac74f481b33bf9579b3c88e9779766baa3f.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>b8c6dac74f481b33bf9579b3c88e9779766baa3f</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\fin-and-ops\get-started\implement-multiple-projects-aad-tenant.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Multiple LCS projects and production environments on one Azure AD tenant</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 つの Azure AD テナントにおける複数の LCS プロジェクトおよび実稼働環境</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to implement multiple LCS projects and production environments on the same Azure Active Directory tenant.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、複数の LCS プロジェクトと実稼動環境を同じ Azure Active Directory テナント上に実装する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Multiple LCS projects and production environments on one Azure AD tenant</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 つの Azure AD テナントにおける複数の LCS プロジェクトおよび実稼働環境</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>For any new Microsoft Dynamics for Finance and Operations (cloud) project, one Microsoft Dynamics Lifecycle Services (LCS) Implementation project is instantiated on a Microsoft Azure Active Directory (Azure AD) tenant that provides access to one production instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての新しい Microsoft Dynamics for Finance and Operations (クラウド) プロジェクトでは、1 つの Microsoft Dynamics Lifecycle Services (LCS) の実装プロジェクトは、1 つの実稼働インスタンスへのアクセスを可能にする Microsoft Azure Active Directory (Azure AD) テナントでインスタンス化されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>In rare cases, to handle the requirements of a specific implementation, you might require multiple production instances that run in parallel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">まれに、特定の実装の要件を処理するため、並列実行している複数の生産インスタンスが必要になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>By creating multiple LCS projects against the same Azure AD tenant, you can have multiple production instances.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同じ Azure AD テナントに対して複数の LCS プロジェクトを作成することで、複数の実稼動インスタンスを持つことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Here are the most common scenarios where multiple production instances might be required:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複数の生産インスタンスが必要になる場合の最も一般的なシナリオを次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>A global implementation's requirements for data residency, latency, or data volume can't be met by one instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">移住地や待機時間のデータまたはデータ量のグローバル実装の要件は、1 つのインスタンスでは満たされません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Different business units in an organization are implementing Finance and Operations separately as independent applications.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">組織内の異なる部署は、Finance and Operations を独立したアプリケーションとして個別に実行しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Manual intervention by the Microsoft Dynamics Service Engineering (DSE) team is required in order to create additional LCS projects on a shared Azure AD tenant.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics サービス エンジニアリング (DSE) チームによる手動操作は、共有 Azure AD テナントで追加の LCS プロジェクトを作成するために必要になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>This approach should be used only if a single-instance strategy truly isn't feasible.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このアプローチは、単一インスタンスの戦略が本当に実現可能でない場合にのみ使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Before additional LCS projects can be created, customers must provide the business justification and confirm that they understand all the implications of the approach.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加の LCS プロジェクトを作成する前に、業務の妥当性を指定し、アプローチのすべての影響を理解していることを確認する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>This process should be started as early in the implementation lifecycle as possible.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロセスは、可能な限り実装ライフサイクルの早い段階で開始する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Customers who decide to proceed should inform the FastTrack solution architect who is assigned to their project that they require additional LCS projects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">続行する場合は、追加の LCS プロジェクトを必要としているプロジェクトに誰が割り当てられているかを、FastTrack ソリューション アーキテクトに通知する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>If no solution architect is assigned to their project, customers should open a support ticket.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション アーキテクトがプロジェクトに割り当てられていない場合、顧客は、サポート チケットを開く必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Licensing requirements</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ライセンス要件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Every LCS Implementation project that runs on the same Azure AD tenant must satisfy the minimum licensing requirements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同じ Azure AD テナント上で実行されるすべての LCS 実装プロジェクトでは、ライセンス契約の最小要件を満たす必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>For example, if there are three LCS Implementation projects on the same Azure AD tenant, a customer must purchase no less than three times the minimum number of subscription licenses.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、同じ Azure AD テナントに 3 つの LCS 実装プロジェクトがある場合、顧客は最低限のサブスクリプション ライセンス数の 3 倍以上を購入する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Currently, the minimum license requirement is 20 full user licenses.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在、ライセンスの最少要件は 20 のユーザー フルライセンスです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Therefore, to run three LCS Implementation projects on the same Azure AD tenant, the customer must purchase at least 60 licenses.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、同じ Azure AD テナントで 3 つの LCS 実装プロジェクトを実行するには、少なくとも 60 ライセンスを購入する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Because the licenses are associated with the Azure AD tenant, the <bpt id="p1">**</bpt>Subscriptions available<ept id="p1">**</ept> page for every LCS project will show the total number of licenses, even though a given LCS project can use only the portion of licenses that has been allocated to it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ライセンスは Azure AD テナントに関連付けられているため、付与された LCS プロジェクトは割り当てられた数量のライセンスしか使えませんが、すべての LCS プロジェクトの<bpt id="p1">**</bpt>利用可能なサブスクリプション<ept id="p1">**</ept>ページでは、ライセンスの総数が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>This allocation of license to LCS projects must be documented outside the system.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この LCS プロジェクトへのライセンス配分は、システム外で文書化する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Users who access multiple environments in parallel must be licensed separately for each environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同時に複数の環境にアクセスするユーザーは、環境ごとに個別にライセンスが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>For more licensing information, download the <bpt id="p1">[</bpt>Licensing guide<ept id="p1">](https://go.microsoft.com/fwlink/?LinkId=866544&amp;clcid=0x409)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ライセンスの詳細については、<bpt id="p1">[</bpt>ライセンス ガイド<ept id="p1">](https://go.microsoft.com/fwlink/?LinkId=866544&amp;clcid=0x409)</ept>をダウンロードしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Disadvantages of multiple LCS projects</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複数の LCS プロジェクトの欠点</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>There are some disadvantages to having multiple LCS projects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複数の LCS プロジェクトを持つことにはいくらかの欠点があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Here are some of them:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次にそのいくつかを挙げます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Master data isn't shared.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マスター データは共有されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Intercompany transactions aren't supported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">会社間トランザクションがサポートされていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Integrations must be configured in each LCS project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">統合は各 LCS プロジェクトで構成される必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Each LCS project requires a separate Bring your own database (BYOD) instance</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各 LCS プロジェクトには、個別の自分のデータベースの持ち込み (BYOD) インスタンスが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>User acceptance testing (UAT) must be done on each instance, even if the code is the same.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードが同じ場合でも、各インスタンスでユーザー受け入れテスト (UAT) を行う必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>UAT is required on each instance, because differences can occur across the LCS projects, even if they share a code base.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード ベースを共有している場合でも、LCS のプロジェクト間で誤差が発生する可能性があるため、各インスタンスに UAT が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>One source of differences can be the integration setup and BYOD configuration that must be done separately in each LCS project and therefore must be tested in each LCS project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">差異の 1 つのソースは LCS プロジェクトごとに個別に実行する必要がある統合設定および BYOD コンフィギュレーションであるため、各 LCS プロジェクトでテストする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Additionally, there might be data variations, different application configurations per region might affect functionality, and different data centers might support a different set of Azure services.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さらに、地域ごとに違うアプリケーション構成が機能に影響する可能性があったり、別のデータ センターが別の Azure サービスのセットをサポートしたりなど、様々なデータ バリエーションがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Microsoft Azure DevOps must be configured in each LCS project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Azure DevOps は各 LCS プロジェクトで構成される必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>When customizations and code are shared, it makes sense to use the same Azure DevOps project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタマイズとコードを共有する場合、同じ Azure DevOps プロジェクトを使用することが理にかなっています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Advantages of multiple LCS projects</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複数の LCS プロジェクトの利点</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>There are also advantages to having multiple LCS projects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複数の LCS プロジェクトを持つことにも利点があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Here are some of them:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次にそのいくつかを挙げます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Data centers can be selected per LCS project to provide the best latency experience.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">待機時間低減のため、LCS プロジェクトごとにデータ センターを選択することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Data centers can be selected per LCS project to satisfy statutory requirements for data residency.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ所在地の法的要件を満たすため、LCS プロジェクトごとにデータ センターを選択することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>There is more flexibility to schedule servicing operations, such as code deployments and upgrades.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードの導入やアップグレードなど、サービス運用のスケジュールを立てることがより柔軟になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Requesting multiple LCS projects on the same Azure AD tenant</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同じ Azure AD テナントで複数の LCS プロジェクトを要求します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>If your solution requires multiple LCS projects on the same Azure AD tenant, all LCS projects except the original project must be provisioned on demand by the DSE team.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューションに同じ Azure AD テナントで複数の LCS プロジェクトが必要になる場合、元のプロジェクトを除くすべての LCS プロジェクトは DSE チームにより必要に応じたプロビジョニングをする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>You should inform the DSE team about this requirement as early as possible, ideally when the project is being onboarded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトがオンボーディングされた時点など、できるだけ早く、この要件について DSE チームに知らせる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>For more information, see <bpt id="p1">[</bpt>Onboard and Finance and Operations project<ept id="p1">](../imp-lifecycle/onboard.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>Finance and Operations のプロジェクト準備<ept id="p1">](../imp-lifecycle/onboard.md)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>To request additional LCS Implementation projects, the customer must create a support request by using the Support portal in LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加の LCS 実装プロジェクトを要求するには、顧客は、LCS でサポート ポータルを使用してサポート リクエストを作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>In this request, the customer must provide the following information:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求では、顧客は次の情報を指定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>The business justification.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">業務の妥当性。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>The enterprise and project structure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンタープライズおよびプロジェクト構造。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>This information includes the following details:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この情報には、次の詳細が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>The name of the Implementation project</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実装プロジェクトの名前</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>The breakdown of licenses per LCS project</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS プロジェクトごとのライセンスの詳細</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Confirmation that the customer understands the implications of multiple LCS projects on the same Azure AD tenant.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同じ Azure AD テナントにおける、複数の LCS プロジェクトの影響を、顧客が理解していることを確認します。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>