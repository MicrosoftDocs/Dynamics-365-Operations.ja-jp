<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="sql-connection-error.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>sql-connection-error.2b8338.5f387c7ae6225951529cdae51be614f467c764ab.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>5f387c7ae6225951529cdae51be614f467c764ab</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\dev-ref\sql-connection-error.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>SQL connection error X++ exception</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ の SQL 接続エラー例外</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes the SQL connection error exception types in X++.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、X++ での SQL 接続エラー例外のタイプについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>SQL connection error X++ exception</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ の SQL 接続エラー例外</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic describes the SQL connection error exception types in X++.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、X++ での SQL 接続エラー例外のタイプについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>TransientSqlConnectionError X++ exception</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TransientSqlConnectionError X++ 例外</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>During an X++ SQL query execution, when a transient SQL connection error occurs on the server side, a TransientSqlConnectionError X++ exception will occur.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ SQL クエリの実行中、サーバー側で一時的な SQL 接続エラーが発生すると、TransientSqlConnectionError X++ 例外が発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Depending on the application requirements, the application should catch and handle the exception.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーションの要件に応じて、アプリケーションは例外をキャッチして処理する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>This exception usually occurs during a large transaction or when the database is under a lot of processing pressure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例外は通常、大規模なトランザクションの際に、またはデータベースに大きな処理負荷がかかっている場合に発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The TransientSqlConnectionError exception is not catchable within the transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TransientSqlConnectionError 例外は、トランザクション内ではキャッチできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The X++ transaction that encounters this exception is canceled (calling <bpt id="p1">**</bpt>ttsAbort<ept id="p1">**</ept>) before the exception occurs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例外が検出された X++ トランザクションは、例外が発生する前にキャンセルされます (<bpt id="p1">**</bpt>ttsAbort<ept id="p1">**</ept> を呼び出す)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>This means that you need to use the catch block to identify the transient SQL connection error instead of a generic X++ error exception, and then retry the outermost transaction or retry application code logic in a new session.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">つまり、汎用 X++ エラー例外ではなく一時的な SQL 接続エラーを特定するためにキャッチ ブロックを使用した後、最上位のトランザクションを再試行するか、新しいセッションでアプリケーション コード ロジックを再試行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>This exception allows the application to be designed for transient server failures.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例外は、一時的なサーバーの障害時にアプリケーションの設計を許可します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>If an application transaction takes a long time to process, you can use multiple incremental delays to catch the TransientSqlConnectionError exception.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション トランザクションの処理に時間がかかる場合、複数の増分遅延を使用して TransientSqlConnectionError 例外をキャッチできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Retrying your application code in a new session is most likely to succeed after you have caught the exception.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいセッションでアプリケーション コードを再実行すると、例外をキャッチした後に成功する可能性が最も高くなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>