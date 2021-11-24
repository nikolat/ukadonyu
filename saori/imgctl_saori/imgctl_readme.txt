=======================================================================
    imgctl.dll
        Version 1.27
        Copyright (C) ルーチェ.
=======================================================================

>> はじめに

 まず、imgctl.dll のダウンロード、ありがとうございます。
 imgctl.dll は、以下の開発環境向けに製作された、画像操作DLLです。

  * Microsoft Visual C++ 6.0/.net/2005/2008
  * Microsoft Visual Basic 6.0
  * Borland C++ Compiler 5.5
  * Borland C++ Builder 5
  * Borland Delphi 6 (Delphi 5 でも恐らくは大丈夫)

 imgctl.dll 及び imgctl.lib は、以下の製品によって作成されました。

  * Visual Studio 2005 Professional Edition (Visual C++ 2005)

 imgctl_bor.lib は、以下のソフトウェアによって作成されました。

  * Borland Implib Version 3.0.22

 その他、使用したコード等は、後述の著作権表記をご覧下さい。

=======================================================================

>> 内容

 以下のファイルが同梱されています

  * imgctl.dll         … DLL本体
  * imgctl.lib         … Visual C++ 用 インポートライブラリ
  * imgctl_bor.lib     … Borland C++ 用 インポートライブラリ

  * imgctl.h           … C/C++ 用 ヘッダファイル
  * imgctl.bas         … Visual Basic 用 関数等定義モジュール
  * imgctl.pas         … Delphi 用 関数等定義ユニット

  * imgctl_util.c      … C/C++ 用 サンプル関数
  * pasteproc.c        … C/C++ 用 PASTEPROC サンプル関数
  * imgctl_util.bas    … Visual Basic 用 サンプル関数
  * pasteproc.bas      … Visual Basic 用 PASTEPROC サンプル関数

  * readme.txt         … このファイル(使用方法等)
  * imgctl.txt         … 関数説明ファイル
  * dibdata.txt        … DIBデータ格納方法説明ファイル

=======================================================================

>> 動作環境

 imgctl.dllはWin32環境向けのDLLです。
 一般的な32ビット(互換)のWindows環境で動作します。
 64ビット環境では動作しません。

 以下の環境での動作をサポートします。

  * Windows 98
  * Windows 98 Second Edition
  * Windows Me
  * Windows 2000
  * Windows XP (32ビット、あるいは32ビット互換)

 Windows 95及びWindows NTはサポートしませんが、動作はします。

=======================================================================

>> 概要

 imgctl.dll では、以下のようなことが出来ます。

  * BMP,RLE-BMP,JPEG,PNG,GIF形式画像ファイルの読み書き(相互変換)。
  * PNG,GIFに関しては高度な設定での保存も可能。
  * アニメーションGIFの保存も可能。
  * DIBデータの24bit(フルカラー)/16bit(ハイカラー)/8bit(256色)化。
  * 256色への減色処理は、市販ソフト程度の品質にはなるかと。
  * DIBデータの色数計算。
  * DIBデータの切り取り、貼り付け(共に上下左右反転自在)。
  * DIBデータの回転(90度単位or任意角度)。
  * DIBデータの淡色化、RGB度合い変更、RGB交換、指定色置換。
  * DIBデータの画面(DC)への転送(内部でAPI関数StretchDIBitsを使用)。
  * 画面(DC)からのDIBデータの取得(上下左右反転自在)。
  * 画像データの形式の割り出し(今後、対応形式を増やしていく予定)。

=======================================================================

>> DLLの使用方法

-----------------------------------------------------------------------

> Visual C++ 6.0/.net/2005/2008 (静的リンクの場合)

 1. プロジェクトのフォルダ内に imgctl.h と imgctl.lib をコピーするか、
    パスの通る位置にこれらのファイルを置いておく。

 2.(6.0の場合)
    メニューの[プロジェクト]→[設定]を選び、設定対象を 全ての構成 に
    して、[リンク]タブの オブジェクト/ライブラリ モジュール の欄に、
    imgctl.lib を書き加える。
   (.netの場合)
    プロジェクトのプロパティを開き、[リンカ]内の[入力]内の、追加する
    依存関係に imgctl.lib を書き加える。

 3. #include "imgctl.h" でヘッダファイルをインクルードする。

 ※ 2.の設定の代わりに #pragma comment(lib, "imgctl.lib") でも可。

-----------------------------------------------------------------------

> Visual Basic 6.0

 プロジェクトに imgctl.bas を標準モジュールとして追加する。

-----------------------------------------------------------------------

> Borland C++ Builder (静的リンクの場合)

 1. プロジェクトフォルダに imgctl.h と imgctl_bor.lib をコピーするか、
    パスの通る位置にこれらのファイルを置いておく。

 2. メニューの[プロジェクト]→[プロジェクトに追加]を選び、
    imgctl_bor.lib をプロジェクトに追加する。

 3. #include "imgctl.h" でヘッダファイルをインクルードする。

 ※ 2.の設定の代わりに #pragma comment(lib, "imgctl_bor.lib") でも可。

 RXF-101さん、情報提供多謝。

-----------------------------------------------------------------------

> Borland Delphi

 1. プロジェクトのあるフォルダに imgctl.pas をコピーするか、Delphi の
    パスの通る場所に imgctl.pas を置いておく。

 2. 使用するユニット中の uses 句に、imgctl を書き加える。

 動的リンクしたい場合は、[プロジェクト]メニューの[オプション]の中の、
 [ディレクトリ/条件]タブの中の条件定義に、IMGCTL_RUNTIME と書く。
 その際、各関数の手続き型が imgctl.pas 内で定義されるが、これが不要な
 場合は、セミコロンで区切って IMGCTL_TYPEDEF_NOTUSE も書き加える。
 そして、API関数 LoadLibrary 及び GetProcAddress を使って呼び出す。

 Delphi はよく知らないので詳しい使い方は割愛。ごめん。

-----------------------------------------------------------------------

> C/C++ (動的リンクの場合)

 #include "imgctl.h" の前に、#define IMGCTL_RUNTIME を書く。
 そして、API関数 LoadLibrary 及び GetProcAddress を使って呼び出す。

   /* (例) PNGtoDIB関数を使用する */

   HMODULE hImgctl;
   PNGTODIB fnP2D;
   HDIB hDIB = NULL;

   hImgctl = LoadLibrary("imgctl.dll");
   if (hImgctl) {
       fnP2D = (PNGTODIB)GetProcAddress(hImgctl, "PNGtoDIB");
       if (fnP2D) { hDIB = fnP2D("image.png"); }
       FreeLibrary(hImgctl);
   }

 関数の型は imgctl.h 内で定義されている(関数名を大文字にしたもの)。
 もしもこれらの型が不要(≒邪魔)ならば、#include "imgctl.h" の前に、
 #define IMGCTL_TYPEDEF_NOTUSE を書く。

 なお、imgctl.h 内の構造体のアラインメントは 4 です。
 v1.12B7 で、アラインメントの違いによってPNGOPT構造体がうまく読めない
 ことがある問題が、構造体自身の修正によって改善されました。

=======================================================================

>> DLLの取り扱い

 imgctl.dll 及びそれに同梱のヘッダファイル等は、全てフリーウェアです。
 imgctl.dll は、あなたが製作したソフトウェア(種別問わず)に自由に同梱
 してくれて構いません。

 同梱したソフトウェアの配布の際に私の許可を得る必要はありません。
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 報告メールを頂けるのは大変嬉しいですが、メール不精なもので返信には
 あまり期待しないで下さい。

 imgctl.dll 単体での転載については、事前に私の許可を得て下さい。

 なお、基本的にフリーウェアですが、シェアウェアや同人ソフト等に使用
 する場合、万が一いくらかの報酬を頂けるというなら、貧乏な作者(私)が
 泣いて喜びます。その場合は、後述の連絡先までご連絡下さい。

 商用利用についても、上述のシェアウェアでの利用時と同じ扱いとします。
 要するに、勝手に使用して頂いて構いません。

 なお、このDLLを使うことによって生じた如何なる障害についても、作者で
 ある私(ルーチェ)は責任を負わないものとします(対応はします)。

=======================================================================

>> 著作権表記

 imgctl.dll は、作者である私(ルーチェ)に著作権があります。
 如何なる場合に於いても、著作権を改竄することは出来ません。

=======================================================================

>> 謝辞

 JPEGの圧縮/解凍部分には、The Independent JPEG Group (IJG) の製作した
 libjpeg を基に宮坂賢さんが作成された
 IJG's JPEG software with x86 SIMD extension を利用しました。
 -> http://cetus.sakura.ne.jp/softlab/jpeg-x86simd/jpegsimd.html

 PNGの圧縮/解凍部分には、libpng 及び zlib を使用しました。
 また、解凍部分は、宮坂賢さん作のSusieプラグイン ifpng.spi のソースを
 参考にしました。

 Version 1.25 における修正では、Toshi Fuku氏提供の修正ソースコード
 およびJPEG関連情報を用いました。

 ライブラリやソースの作者様には、この場を借りて厚く御礼申し上げます。

=======================================================================

>> 余談

 そろそろ imgctl からは手を引いて、ソースコードを一新したライブラリを
 作成したいところです。

 …と書いてから早二年。

=======================================================================

>> 更新履歴 ('*'が多いほど重要な更新です)

> Version 1.00B [2001/12/08]
  **: HRKさんのホームページ(http://www.meteo.ee.vu/)にある動作テスト
      掲示板にて仮公開した(関数説明ファイル無し^_^;)。

> Version 1.00 [2001/12/18]
 ***: 正式リリース。
 ***: HeadDIB, ColorDIB, DIBto16Bit の３関数を追加。
 ***: DIBto24Bit, DIBtoRLE, RLEtoDIB の３関数の仕様を変更。
  **: SizeDIB 関数を削除。

> Version 1.01B [2002/02/03]
 ***: ToDIB, PaletteDIB, PixelDIB, CutDIB, DIBtoPNGex の５関数を追加。
 ***: HeadDIB 関数のバグを修正。

> Version 1.01B2 [2002/02/04]
 ***: ImgctlBeta, DCtoDIB の２関数を追加。

> Version 1.01 [2002/02/06]
   *: DIBtoPNGex 関数の内部仕様を微妙に変更。
  **: imgctl_util.c に DIBtoPNGex 関数の説明を追加。

> Version 1.02B [2002/02/13]
 ***: DIBto8Bit 関数を追加。
 ***: DIBto24Bit, DIBto16Bit の２関数のバグを修正。

> Version 1.02B2 [2002/02/13]
 ***: GrayDIB, ToneDIB, ReplaceDIB の３関数を追加。

> [2002/02/19]
 ***: Borland Delphi 6 に対応した。
   *: imgctl.bas にバージョン情報定数追加。

> Version 1.02 [2002/03/06]
  **: PNGtoDIB 関数の不備を修正。

> Version 1.03B [2002/03/16]
 ***: GetImageType, DIBto8Bit, BMPtoDIB の３関数を拡張。

> Version 1.03B2 [2002/03/17]
 ***: JPGtoDIB 関数を拡張。

> Version 1.03B3 [2002/04/02]
 ***: GetImageType 関数を修正。

> Version 1.03 [2002/04/30]
  **: GetImageType 関数にPCX形式の判別を追加。

> Version 1.04B [2002/05/25]
 ***: GetImageType 関数を修正。

> Version 1.04 [2002/08/04]
 ***: DIBStretchDIBits2 関数を追加。

> Version 1.05B [2002/09/08]
 ***: PasteDIB 関数を追加。
 ***: CutDIB 関数の高さがマイナス時に切り取り範囲が異なる不備を修正。
 ***: DIBDIBits, DIBStretchDIBits, DIBStretchDIBits2 の３関数の転送元の
      切り取り範囲が異なる不備修正。

> Version 1.05 [2002/09/23]
 ***: InfoPNG 関数を追加。

> Version 1.06B [2002/10/10]
 ***: TurnDIB 関数を追加。
   *: CutDIB 関数を微修正。
  **: 異なるバージョン間での互換を持たせた(v1.05以降)。

> Version 1.06 [2002/11/12]
 ***: RepaintDIB 関数を追加。
   *: ヘッダファイル等でのタイプミス、スペルミスを修正。

> Version 1.07B [2002/11/25]
  **: GetImageType 関数のJPEG形式の判別を微修正。
  **: DIBDIBits, DIBStretchDIBits, DIBStretchDIBits2 の３関数の座標の
      自動補正を削除(よりAPI関数に近くした)。

> Version 1.07B2 [2003/01/23]
 ***: ImgctlError, ImgctlErrorClear の２関数を追加。
 ***: PixelDIB 関数の、RLE-DIBだと色を取得出来ないバグを修正。
  **: GetDIB 関数の処理を修正(imgctl.txt参照)。

> [2003/01/23]
  **: Visual C++ .net に対応した。
  **: Visual C++ .net でコンパイルした(実行速度向上)。

> Version 1.07B3 [2003/01/26]
 ***: ImgctlError 関数のエラーコードを追加。
 ***: HDIB型を引数に取る関数のNULLチェック処理を追加。
  **: ファイル名を引数に取る関数のNULLチェック処理を追加。
 ***: 各関数の引数における不正なNULLのチェック処理を追加。
 ***: Visual C# .net にとりあえず対応した。

> Version 1.07 [2003/02/10]
  **: JPEGライブラリ及びPNGライブラリを再構築した。

> Version 1.08B [2003/03/10] (v1.08に誤設定)
  **: PointerOf 関数を追加。(Visual Basic 向けの関数です)
   *: バージョン文字列定数 IMGCTL_VERSION_STRING を追加。
  **: imgctl.bas の BITMAPINFO データ型を修正。
  **: imgctl_util.bas に DIBtoPNGex 関数の説明を追加。
  **: C++ 用クラス ccImage が記述された imgctl_class.h を追加。

> Version 1.08B2 [2003/03/10]
 ***: DataDIB, DIBtoDC, DIBtoDCex, DIBtoDCex2 の４関数を追加。
 ***: メモリの確保方法を malloc から GlobalAlloc に変更。
 ***: DIBデータ格納方法についての説明ファイル dibdata.txt 追加。
  **: imgctl_class.h を正式追加(前バージョンは誤設定有り)。
  **: imgctl.pas の構文ミスを修正(汗)。

> Version 1.08 [2003/03/10]
 ***: DataDIB 関数仕様変更。
 ***: メモリの確保方法を GlobalAlloc から malloc に戻した(汗)。

> Version 1.09 [2003/03/15]
 ***: DIBtoDC, DIBtoDCex の２関数の仕様を大幅修正。
      これらの関数を内部で利用する以下の関数にも影響します。
      DIBtoDCex2, DIBDIBits, DIBStretchDIBis, DIBStretchDIBits2
  **: 上の修正に伴い、ImgctlError 関数のエラーコードを追加。
  **: DIBtoPNGex 関数での透過色指定のバグ修正。

> Version 1.10B [2003/03/20]
 ***: DIBtoDC, DIBtoDCex の２関数の仕様を修正。
      これらの関数を内部で利用する以下の関数にも影響します。
      DIBtoDCex2, DIBDIBits, DIBStretchDIBis, DIBStretchDIBits2
 ***: PasteDIB 関数のバグと仕様を修正、及び機能拡張。
  **: 上の修正に伴い、ImgctlError 関数のエラーコードを追加。
  **: pasteproc.c, pasteproc.bas のサンプル関数追加。

> Version 1.10B2 [2003/03/25]
  **: GetImageType 関数で、PIC形式とPICT形式を混同していた(汗)。
      定数より、IMG_PICT 及び IMG_PCT をコメントアウト。

> Version 1.10B3 [2003/03/25]
  **: DIBtoJPG, JPGtoDIB, DIBtoPNG, DIBtoPNGex の４関数を拡張。
   *: PNGtoDIB, InfoPNG の２関数を修正。

> Version 1.10B4 [2003/03/26]
 ***: DIBto16BitEx 関数を追加。
 ***: GetImageType, CreateDIB, DIBto8Bit の３関数を拡張。
   *: DIBto16Bit, BMPtoDIB の２関数を微修正。
  **: 16Bit, 32Bit の色変換処理を修正。

> Version 1.10B5 [2003/03/27]
  **: DIBto16BitEx, DIBto8Bit の２関数を拡張。

> Version 1.10B6 [2003/03/27]
 ***: DIBto16BitEx, DIBto8Bit の２関数を修正及び拡張。

> Version 1.10B7 [2003/03/27]
 ***: DIBto16BitEx, DIBto8Bit の２関数を仕様変更、修正、及び拡張。

> Version 1.10B8 [2003/03/28]
   *: DIBto16BitEx, DIBto8Bit の２関数を拡張。

> Version 1.10 [2003/03/29]
   *: DIBto16BitEx, DIBto8Bit の２関数を仕様変更。

> Version 1.11B [2003/03/30]
   *: DeleteDIB 関数を微修正。
  **: 内部利用の libpng.lib 及び zlib.lib をバージョンアップ。

> Version 1.11 [2003/04/02]
 ***: DIBtoJPG 関数が必ず失敗するという致命的バグ修正。
  **: imgctl_util.bas の構文間違いを修正。

> Version 1.12B [2003/04/06]
 ***: ResizeDIB 関数を追加。
  **: InfoPNG 関数のパレット取得処理のバグ修正。

> Version 1.12B2 [2003/04/06]
 ***: GammaDIB, ContrastDIB の２関数を追加。
 ***: ResizeDIB 関数の拡大処理を改善。

> Version 1.12B3 [2003/04/07]
 ***: TableDIB, ShadeDIB の２関数を追加。
 ***: GammaDIB, ContrastDIB の２関数を仕様変更。
  **: CreateDIB 関数を拡張、及び内部仕様変更。
   *: ToneDIB 関数の内部仕様変更。
  **: ImgctlError 関数のエラーコードを追加。

> Version 1.12B4 [2003/04/15]
 ***: TurnDIBex 関数を追加。

> Version 1.12B4f [2003/04/21]
  **: DataDIB 関数を修正(C/C++のみ)。
  **: 上に伴い、IMGDATA 構造体メンバのconst指定を除外(C/C++のみ)。

> Version 1.12B4f2 [2003/05/07]
 ***: RepaintDIB のDLL呼び出しを修正(VBのみ)。

> Version 1.12B5 [2003/05/18]
 ***: PNGAtoDIB 関数を追加。
  **: PNGtoDIB 関数の内部仕様変更。
  **: ImgctlError 関数のエラーコードを追加。
  **: pasteproc.c のサンプル関数追加。

> Version 1.12B6 [2003/06/11]
  **: DIBtoPNGex 関数の透過処理を修正。

> Version 1.12B7 [2003/06/12]
 ***: DIBtoPNGex 関数の透過処理を修正。
  **: 構造体にアラインメントを指定。
  **: PNGOPT 構造体にアラインメント用ダミー変数追加。

> Version 1.12B8 [2003/06/21]
 ***: DIBtoJPG 関数で失敗時にファイルクローズされないバグを修正。
 ***: JPGtoDIB 関数で失敗時にファイルクローズされないバグを修正。
   *: imgctl.bas のバージョン定数が古かったミスを修正。

> Version 1.12B9 [2003/07/15]
 ***: GetImageType 関数の仕様変更。
  **: imgctl.cs 及び imgctl.bas の手直し。

> Version 1.12B10 [2003/09/07]
  **: GetImageType 関数のJPEG形式の判別を微修正。

> Version 1.12 [2003/11/26]
   *: DIBtoBMP 関数の不可思議な処理を削除。

> [2003/12/02]
  **: imgctl.bas の文法ミスを修正。

> Version 1.13B [2003/12/12]
  **: JPGtoDIB 関数でCMYK色空間のJPEGを読み込めるようになった。

> Version 1.13B2 [2003/12/18]
  **: 試験的に DIBtoJPG 関数の内部仕様を変更。(imgctl.txt参照)

> Version 1.13B3 [2004/04/20]
   *: JPGtoDIB 関数で解像度が変な値に設定されることがあるのを修正。

> Version 1.13B4 [2004/06/21]
 ***: DIBtoGIF, DIBtoGIFex, GIFtoDIB, GIFtoDIBex の４関数を追加。
   *: C#言語への対応を止め、imgctl.cs を撤去。
   *: C++クラス imgctl_class.h を撤去。

> Version 1.13 [2004/06/23]
 ***: DIBtoGIFAni, DIBtoGIFAniEx の２関数を追加。

> Version 1.14 [2004/07/03]
 ***: GIFtoDIB, GIFtoDIBex の２関数の致命的なバグを修正。

> [2004/07/04]
   *: サンプルをいくつか書き換えた。

> Version 1.15 [2004/08/24]
 ***: DIBto24Bit 関数で32ビットDIBが正常に変換できないバグを修正。
  **: 試験的に DIBto8Bit 関数の内部仕様を変更。(imgctl.txt参照)

> Version 1.16B [2004/08/30]
  **: 内部利用の libpng.lib 及び zlib.lib をバージョンアップ。

> Version 1.16B2 [2004/09/11]
 ***: PNG画像が正常に作成されなくなっていたバグを修正。
   *: 内部利用の libpng.lib をバージョンアップ。

> [2004/09/30]
 ***: imgctl.pas の文法ミスを修正。

> Version 1.16B3 [2005/01/18]
 ***: BMPMtoDIB, JPGMtoDIB, PNGMtoDIB, PNGMAtoDIB, InfoPNGM,
      GIFMtoDIB, GIFMtoDIBex の７関数を追加。
  **: ImgctlError 関数のエラーコードを追加。

> Version 1.16B4 [2005/01/28]
 ***: 内部利用の libpng.lib にαチャンネル付きPNGを読み込めないバグが
      あったため、最新版にバージョンアップ。

> Version 1.16B5 [2005/02/01]
 ***: GIF書き出し系関数で不正な 0 を書き出すことがあったバグを修正。

> Version 1.16 [2005/02/01]
 ***: GetImageMType, MtoDIB の２関数を追加。
  **: GetImageType 関数の内部仕様を変更。

> Version 1.17 [2005/02/03]
 ***: GIF読み込み系関数のバグを修正。

> Version 1.18 [2005/04/20]
 ***: BMPtoDIB 関数を修正。
 ***: TurnDIB 関数で1,4ビットDIB回転時に乱れが生じるバグを修正。

> Version 1.19 [2005/06/14]
 ***: PNGtoDIB, PNGMtoDIB の２関数の2ビットPNG読み込みバグを修正。

> Version 1.20 [2005/07/26]
 ***: DIBtoGIFex, DIBtoGIFAniEx の２関数の透過色に関するバグを修正。

> Version 1.21 [2006/02/04]
 ***: BMPtoDIB, BMPMtoDIB の２関数のビットフィールドBMPが読み込めない
      バグを修正。
 ***: DIBtoRLE 関数でうまくRLE変換されないことがあったバグを修正。
 ***: CutDIB 関数でビットフィールドBMPのタイプが書き換えられてしまう
      バグを修正。
   *: imgctl.txt の表記ミスを修正。

> Version 1.22 [2006/02/05]
 ***: BMPtoDIB, BMPMtoDIB の２関数のビットフィールドBMPが読み込めない
      バグを今度こそ修正。

> Version 1.23 [2006/03/26]
  **: ResizeDIB 関数の拡大処理の内部仕様を変更。

> Version 1.24 [2007/02/27]
  **: 内部利用のJPEGライブラリをIJG標準の libjpeg から
      IJG's JPEG software with x86 SIMD extension に変更。
   *: 内部利用の libpng 及び zlib をバージョンアップ。

> Version 1.25 [2009/02/19]
 ***: 不正なJPEG読み込みでフリーズするバグを修正。
 ***: GIF読み込みでフリーズする可能性があるバグの修正。
 ***: ゼロ除算が起きうる関数を修正。
  **: GetImageType 関数でV4,V5タイプのBMPを認識できるように修正。
   *: JPEGライブラリのコード削減策を適用した。
   *: 内部利用の libpng をバージョンアップ。
   *: ビルド環境を Visual Studio 2005 に変更(…の影響かサイズ増大)。

> Version 1.26 [2009/04/06]
 ***: RGB形式のJPEGを読み込むとRとBが反転してしまうバグを修正。
  **: Adobe Photoshop でCMYK形式で保存したJPEGの読み込みに仮対応。
  **: 不正なGIF画像を読み込むとフリーズする場合があるバグを修正。

> Version 1.27 [2010/03/06]
 ***: 内部利用の libpng をバージョンアップ(脆弱性対策の為)。

=======================================================================

>> 連絡先

 ルーチェ's Homepage [作者サイト]
     http://www.ruche-home.net/

 メールアドレス [サポート用]
     info@ruche-home.net

=======================================================================
README  2010-03-06  by ruche.