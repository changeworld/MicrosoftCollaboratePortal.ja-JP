---
title: パッケージの操作をダウンロードします。
description: Microsoft の共同作業のパッケージは、ダウンロードの利用可能なファイルを含み、契約に関連付けられました。 配布マネージャーは、複数ファイルまたは一括のダウンロードを実行します。
author: ikhapova
ms.author: ikhapova
ms.date: 12/12/2017
keywords: パッケージでは、契約、パッケージのダウンロード、ダウンロード、ビルド、共同作業のアクセス許可は、Microsoft Connect
ms.openlocfilehash: 25a89feaf8d71be3cde4393042f1bf0e8047c765
ms.sourcegitcommit: 8ae2ead732e03d8a9865797bb9f40818780036e9
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/16/2018
ms.locfileid: "43054679"
---
# <a name="working-with-packages-to-download-content"></a>コンテンツをダウンロードするパッケージの操作

Microsoft の共同作業 (MS 共同作業) でダウンロード可能なコンテンツとして利用*パッケージ*ダウンロードするファイルが含まれています。  パッケージには、発行日付、およびキーワードの説明、パッケージの種類など、適切なパッケージの検索を容易に関連するメタデータがあります。   

属しているパッケージをダウンロードすることができますが、エンゲージメントに依存します。  、発行時に、コンテンツ発行者は、パッケージの特定のサービスを対象します。 場合は、engagement の構成要素のメンバーでは、その engagement 用のパッケージを参照してください。 できなきます。  これは、ユーザーは所属する契約に関連付けられているパッケージのみを表示できることを意味します。

MS の共同作業には、コンテンツのパッケージをダウンロードするための 2 つのメカニズムが用意されています。
1. MS の共同作業**ポータルの [パッケージ] ページ**パッケージを見つけて、個々 のファイルをパッケージからダウンロードすることができます。 
2. MS の共同作業**配布マネージャー**一度に複数のファイルとパッケージをダウンロードするローカル コンピューターにインストールできます。

使用するダウンロード メカニズムに関係なく、配布マネージャーのように、ポータルで同じパッケージが表示されます。

コンテンツの発行元は、契約に関連付けられている MS 共同作業の権限ロールです。  この時点では、Microsoft ユーザーのみが契約を発行できます。 Engagement の所有者は、ユーザーがコンテンツの発行元のアクセス許可を持ってを定義します。

## <a name="finding-packages-in-the-ms-collaborate-portal"></a>MS の共同作業ポータルでのパッケージの検索

**パッケージ**フィルター処理できます ページとを含む複数の条件に基づいてパッケージの検索。
- 名前、内の単語 
- プログラムまたはパッケージが含まれている活動 
- パッケージの発行 
- パッケージ内に、ファイルの種類と
- キーワードを使用します。

たとえば、特定の Windows のビルド パッケージを探しているビルド番号がある場合は、フィルターとして入力できます。 少ないフィルターを使用して開始し、パッケージの数を制限する探しているものが見つかるまでを返されます。 さらに追加できるように、各フィルターのボックスは、累積的です。 パッケージの一覧をパッケージを検索するための列で並べ替えることもできます。

配布マネージャーが、基本的な検索や並べ替え機能が豊富な検索とフィルター操作性が設定されています。  使用できる多くのパッケージがある場合は、ポータルの検索を使用して、適切なパッケージを検索し、配布マネージャーにパッケージ名を検索することをお勧めします。

## <a name="how-to-download-files-from-the-ms-collaborate-portal"></a>MS の共同作業ポータルからファイルをダウンロードする方法

1. ダッシュ ボードで、クリックを取得するには、「パッケージ」、**パッケージ** ページで、ダウンロード可能なすべてのパッケージの一覧が表示されます。

2. 検索するかを使用して、**高度なフィルター**をダウンロードするには、パッケージを検索します。 フィルターは、検索を絞り込むに累積されます。 すべてのフィルターを削除するのにには、"フィルターをクリア ボタンを使用します。
    - をクリックして、**高度なフィルター**高度なフィルターの表示を切り替えるアイコン"フィールド。
    ![高度なフィルターのアイコン](images/package-advanced-filter.png)
3. ダウンロードするパッケージを検索するときは、パッケージを開くことをクリックします。 すべてのパッケージに関する詳細とダウンロード可能なファイルの一覧が表示されます。
    ![パッケージの詳細 ウィンドウ](images/package-details.png)

4. ダウンロードを開始するには、各ファイルをクリックします。 MS の共同作業ポータルでは、一度に 1 つのファイルをダウンロードできます。 

## <a name="using-distribution-manager-for-multi-file-downloads"></a>配布マネージャーを使用して、複数ファイルのダウンロード

複数のファイルの完全なパッケージまたは大きなパッケージをダウンロードする場合をインストールするお勧め、**配布マネージャー**します。  配布マネージャーとは、必要に応じて更新する ClickOnce クライアント アプリケーションです。  

このクライアント アプリケーションは、MS の共同作業を MS の共同作業ポータルにログインするときと同じ資格情報を使用してサービスに接続します。 配布マネージャーに MS の共同作業ポータルでご覧同じパッケージをすべて表示されます。

一度に複数のファイルをダウンロードするだけでなく、バック グラウンドで実行する多くのパッケージをキューに配置でき、接続の問題に対処するダウンロードの設定をカスタマイズすることもできます。

### <a name="how-to-install-the-distribution-manager"></a>配布マネージャーをインストールする方法

1. **パッケージ** ページで、をクリックして、**配布マネージャー**ページの上部にあるボタンをクリックします。 
    ![配布マネージャーのインストール パッケージ ページ](images/Distribution-Mgr-Launch.PNG)

2. をクリックして**オープン**クリックしてメッセージ**インストール** ダイアログ ボックスでアプリケーションをインストールします。 

既にログインしている、デベロッパー センター Distributuion Manager ボタンをクリックすると、配布マネージャーは起動し、MS の共同作業へのログインを使用した同じアカウントでサインインします。

### <a name="how-to-log-in-to-distribution-manager"></a>配布マネージャーにログインする方法

配布マネージャーは、MS の共同作業に使用する同じアカウントを使用します。  を、MS Collaborfate ポータルから起動する場合はログインする必要が自動的にします。  MS 共同作業に既にログインしていないこと、サイトにアクセスする、MSA アカウントを使用している場合や、配布マネージャーにもう一度ログインする必要があります。 これは、同じアカウントと MS の共同作業ポータルにログインするために使用するプロセスに使用されます。

1.  選択して、コンピューター上の配布マネージャー アプリケーションを起動、**配布マネージャー**のボタンでは、**パッケージ**またはに移動して、MS の共同作業ポータルでページ**配布マネージャー**コンピューターのアプリケーションの一覧にします。

2.  デベロッパー センター、または MS の共同作業にログインするときに表示 画面で、同じログが表示されます。 適切なアカウントを選択し、パスワードを入力、配布マネージャーは、MS の共同作業アカウントに接続します。

### <a name="how-to-download-packages-using-distribution-manager"></a>配布マネージャーを使用してパッケージをダウンロードする方法

1.  配布マネージャーには、検索機能を使用してパッケージまたはパッケージ一覧をスクロールして検索します。
2.  パッケージ内の複数のファイルまたは複数のパッケージをダウンロードするを選択することができます。  最大で 4 つのパッケージを一度にダウンロードできます。
3.  使用してダウンロードするには、フォルダーを選択することができます、**参照**ボタンをクリックします。
4.  クリックして**ダウンロード**を選択したパッケージのダウンロードを開始します。
5.  アイコンは、ダウンロードのキューに置かれたパッケージのステータスを示すために更新します。

あるファイルが表示されます**今すぐダウンロード**およびダウンロードのキューに置かれたパッケージ。  クリックすることができます**今すぐダウンロード**をダウンロードするファイルのみを参照してください。  

移動することもできます。**を今すぐダウンロード チェック**配布マネージャーのメニューから。

   ![[パッケージ] ページで [今すぐダウンロード] メニュー項目のチェック](images/check-for-downloads.png)

> [!NOTE]
> - できます**ダウンロードを一時停止**およびダウンロードを続行し、再開します。
> - メニュー項目をクリックして選択し、配布マネージャーの同期を強制できます**を今すぐダウンロード チェック**します。
> - クリックすると**設定** メニューから使用すると、カスタマイズを行います。 

### <a name="customizing-distribution-manager-settings"></a>配布マネージャーの設定をカスタマイズします。

配布マネージャーにアクセスできます**設定**ログイン名の近くのメニューから。  配布マネージャーの設定は、パッケージのダウンロードを取得する方法をカスタマイズできます。  次の設定を調整できます。
- ブロックのサイズ 
- スレッドをダウンロードし、
- 最大速度が向上します。

のみを変更するこれらのダウンロードに関する、低速または信頼性の低い接続が原因になる可能性がある問題が発生している場合をお勧めします。

![配布マネージャーの設定をカスタマイズします。](images/Distribution-Mgr-Settings.PNG)
