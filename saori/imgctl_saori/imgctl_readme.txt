=======================================================================
    imgctl.dll
        Version 1.27
        Copyright (C) ���[�`�F.
=======================================================================

>> �͂��߂�

 �܂��Aimgctl.dll �̃_�E�����[�h�A���肪�Ƃ��������܂��B
 imgctl.dll �́A�ȉ��̊J���������ɐ��삳�ꂽ�A�摜����DLL�ł��B

  * Microsoft Visual C++ 6.0/.net/2005/2008
  * Microsoft Visual Basic 6.0
  * Borland C++ Compiler 5.5
  * Borland C++ Builder 5
  * Borland Delphi 6 (Delphi 5 �ł����炭�͑��v)

 imgctl.dll �y�� imgctl.lib �́A�ȉ��̐��i�ɂ���č쐬����܂����B

  * Visual Studio 2005 Professional Edition (Visual C++ 2005)

 imgctl_bor.lib �́A�ȉ��̃\�t�g�E�F�A�ɂ���č쐬����܂����B

  * Borland Implib Version 3.0.22

 ���̑��A�g�p�����R�[�h���́A��q�̒��쌠�\�L�������������B

=======================================================================

>> ���e

 �ȉ��̃t�@�C������������Ă��܂�

  * imgctl.dll         �c DLL�{��
  * imgctl.lib         �c Visual C++ �p �C���|�[�g���C�u����
  * imgctl_bor.lib     �c Borland C++ �p �C���|�[�g���C�u����

  * imgctl.h           �c C/C++ �p �w�b�_�t�@�C��
  * imgctl.bas         �c Visual Basic �p �֐�����`���W���[��
  * imgctl.pas         �c Delphi �p �֐�����`���j�b�g

  * imgctl_util.c      �c C/C++ �p �T���v���֐�
  * pasteproc.c        �c C/C++ �p PASTEPROC �T���v���֐�
  * imgctl_util.bas    �c Visual Basic �p �T���v���֐�
  * pasteproc.bas      �c Visual Basic �p PASTEPROC �T���v���֐�

  * readme.txt         �c ���̃t�@�C��(�g�p���@��)
  * imgctl.txt         �c �֐������t�@�C��
  * dibdata.txt        �c DIB�f�[�^�i�[���@�����t�@�C��

=======================================================================

>> �����

 imgctl.dll��Win32��������DLL�ł��B
 ��ʓI��32�r�b�g(�݊�)��Windows���œ��삵�܂��B
 64�r�b�g���ł͓��삵�܂���B

 �ȉ��̊��ł̓�����T�|�[�g���܂��B

  * Windows 98
  * Windows 98 Second Edition
  * Windows Me
  * Windows 2000
  * Windows XP (32�r�b�g�A���邢��32�r�b�g�݊�)

 Windows 95�y��Windows NT�̓T�|�[�g���܂��񂪁A����͂��܂��B

=======================================================================

>> �T�v

 imgctl.dll �ł́A�ȉ��̂悤�Ȃ��Ƃ��o���܂��B

  * BMP,RLE-BMP,JPEG,PNG,GIF�`���摜�t�@�C���̓ǂݏ���(���ݕϊ�)�B
  * PNG,GIF�Ɋւ��Ă͍��x�Ȑݒ�ł̕ۑ����\�B
  * �A�j���[�V����GIF�̕ۑ����\�B
  * DIB�f�[�^��24bit(�t���J���[)/16bit(�n�C�J���[)/8bit(256�F)���B
  * 256�F�ւ̌��F�����́A�s�̃\�t�g���x�̕i���ɂ͂Ȃ邩�ƁB
  * DIB�f�[�^�̐F���v�Z�B
  * DIB�f�[�^�̐؂���A�\��t��(���ɏ㉺���E���]����)�B
  * DIB�f�[�^�̉�](90�x�P��or�C�ӊp�x)�B
  * DIB�f�[�^�̒W�F���ARGB�x�����ύX�ARGB�����A�w��F�u���B
  * DIB�f�[�^�̉��(DC)�ւ̓]��(������API�֐�StretchDIBits���g�p)�B
  * ���(DC)�����DIB�f�[�^�̎擾(�㉺���E���]����)�B
  * �摜�f�[�^�̌`���̊���o��(����A�Ή��`���𑝂₵�Ă����\��)�B

=======================================================================

>> DLL�̎g�p���@

-----------------------------------------------------------------------

> Visual C++ 6.0/.net/2005/2008 (�ÓI�����N�̏ꍇ)

 1. �v���W�F�N�g�̃t�H���_���� imgctl.h �� imgctl.lib ���R�s�[���邩�A
    �p�X�̒ʂ�ʒu�ɂ����̃t�@�C����u���Ă����B

 2.(6.0�̏ꍇ)
    ���j���[��[�v���W�F�N�g]��[�ݒ�]��I�сA�ݒ�Ώۂ� �S�Ă̍\�� ��
    ���āA[�����N]�^�u�� �I�u�W�F�N�g/���C�u���� ���W���[�� �̗��ɁA
    imgctl.lib ������������B
   (.net�̏ꍇ)
    �v���W�F�N�g�̃v���p�e�B���J���A[�����J]����[����]���́A�ǉ�����
    �ˑ��֌W�� imgctl.lib ������������B

 3. #include "imgctl.h" �Ńw�b�_�t�@�C�����C���N���[�h����B

 �� 2.�̐ݒ�̑���� #pragma comment(lib, "imgctl.lib") �ł��B

-----------------------------------------------------------------------

> Visual Basic 6.0

 �v���W�F�N�g�� imgctl.bas ��W�����W���[���Ƃ��Ēǉ�����B

-----------------------------------------------------------------------

> Borland C++ Builder (�ÓI�����N�̏ꍇ)

 1. �v���W�F�N�g�t�H���_�� imgctl.h �� imgctl_bor.lib ���R�s�[���邩�A
    �p�X�̒ʂ�ʒu�ɂ����̃t�@�C����u���Ă����B

 2. ���j���[��[�v���W�F�N�g]��[�v���W�F�N�g�ɒǉ�]��I�сA
    imgctl_bor.lib ���v���W�F�N�g�ɒǉ�����B

 3. #include "imgctl.h" �Ńw�b�_�t�@�C�����C���N���[�h����B

 �� 2.�̐ݒ�̑���� #pragma comment(lib, "imgctl_bor.lib") �ł��B

 RXF-101����A���񋟑��ӁB

-----------------------------------------------------------------------

> Borland Delphi

 1. �v���W�F�N�g�̂���t�H���_�� imgctl.pas ���R�s�[���邩�ADelphi ��
    �p�X�̒ʂ�ꏊ�� imgctl.pas ��u���Ă����B

 2. �g�p���郆�j�b�g���� uses ��ɁAimgctl ������������B

 ���I�����N�������ꍇ�́A[�v���W�F�N�g]���j���[��[�I�v�V����]�̒��́A
 [�f�B���N�g��/����]�^�u�̒��̏�����`�ɁAIMGCTL_RUNTIME �Ə����B
 ���̍ہA�e�֐��̎葱���^�� imgctl.pas ���Œ�`����邪�A���ꂪ�s�v��
 �ꍇ�́A�Z�~�R�����ŋ�؂��� IMGCTL_TYPEDEF_NOTUSE ������������B
 �����āAAPI�֐� LoadLibrary �y�� GetProcAddress ���g���ČĂяo���B

 Delphi �͂悭�m��Ȃ��̂ŏڂ����g�����͊����B���߂�B

-----------------------------------------------------------------------

> C/C++ (���I�����N�̏ꍇ)

 #include "imgctl.h" �̑O�ɁA#define IMGCTL_RUNTIME �������B
 �����āAAPI�֐� LoadLibrary �y�� GetProcAddress ���g���ČĂяo���B

   /* (��) PNGtoDIB�֐����g�p���� */

   HMODULE hImgctl;
   PNGTODIB fnP2D;
   HDIB hDIB = NULL;

   hImgctl = LoadLibrary("imgctl.dll");
   if (hImgctl) {
       fnP2D = (PNGTODIB)GetProcAddress(hImgctl, "PNGtoDIB");
       if (fnP2D) { hDIB = fnP2D("image.png"); }
       FreeLibrary(hImgctl);
   }

 �֐��̌^�� imgctl.h ���Œ�`����Ă���(�֐�����啶���ɂ�������)�B
 �����������̌^���s�v(���ז�)�Ȃ�΁A#include "imgctl.h" �̑O�ɁA
 #define IMGCTL_TYPEDEF_NOTUSE �������B

 �Ȃ��Aimgctl.h ���̍\���̂̃A���C�������g�� 4 �ł��B
 v1.12B7 �ŁA�A���C�������g�̈Ⴂ�ɂ����PNGOPT�\���̂����܂��ǂ߂Ȃ�
 ���Ƃ������肪�A�\���̎��g�̏C���ɂ���ĉ��P����܂����B

=======================================================================

>> DLL�̎�舵��

 imgctl.dll �y�т���ɓ����̃w�b�_�t�@�C�����́A�S�ăt���[�E�F�A�ł��B
 imgctl.dll �́A���Ȃ������삵���\�t�g�E�F�A(��ʖ�킸)�Ɏ��R�ɓ���
 ���Ă���č\���܂���B

 ���������\�t�g�E�F�A�̔z�z�̍ۂɎ��̋��𓾂�K�v�͂���܂���B
 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 �񍐃��[���𒸂���̂͑�ϊ������ł����A���[���s���Ȃ��̂ŕԐM�ɂ�
 ���܂���҂��Ȃ��ŉ������B

 imgctl.dll �P�̂ł̓]�ڂɂ��ẮA���O�Ɏ��̋��𓾂ĉ������B

 �Ȃ��A��{�I�Ƀt���[�E�F�A�ł����A�V�F�A�E�F�A�⓯�l�\�t�g���Ɏg�p
 ����ꍇ�A�����ꂢ���炩�̕�V�𒸂���Ƃ����Ȃ�A�n�R�ȍ��(��)��
 �����Ċ�т܂��B���̏ꍇ�́A��q�̘A����܂ł��A���������B

 ���p���p�ɂ��Ă��A��q�̃V�F�A�E�F�A�ł̗��p���Ɠ��������Ƃ��܂��B
 �v����ɁA����Ɏg�p���Ē����č\���܂���B

 �Ȃ��A����DLL���g�����Ƃɂ���Đ������@���Ȃ��Q�ɂ��Ă��A��҂�
 ���鎄(���[�`�F)�͐ӔC�𕉂�Ȃ����̂Ƃ��܂�(�Ή��͂��܂�)�B

=======================================================================

>> ���쌠�\�L

 imgctl.dll �́A��҂ł��鎄(���[�`�F)�ɒ��쌠������܂��B
 �@���Ȃ�ꍇ�ɉ����Ă��A���쌠����₂��邱�Ƃ͏o���܂���B

=======================================================================

>> �ӎ�

 JPEG�̈��k/�𓀕����ɂ́AThe Independent JPEG Group (IJG) �̐��삵��
 libjpeg ����ɋ{�⌫���񂪍쐬���ꂽ
 IJG's JPEG software with x86 SIMD extension �𗘗p���܂����B
 -> http://cetus.sakura.ne.jp/softlab/jpeg-x86simd/jpegsimd.html

 PNG�̈��k/�𓀕����ɂ́Alibpng �y�� zlib ���g�p���܂����B
 �܂��A�𓀕����́A�{�⌫������Susie�v���O�C�� ifpng.spi �̃\�[�X��
 �Q�l�ɂ��܂����B

 Version 1.25 �ɂ�����C���ł́AToshi Fuku���񋟂̏C���\�[�X�R�[�h
 �����JPEG�֘A����p���܂����B

 ���C�u������\�[�X�̍�җl�ɂ́A���̏���؂�Č������\���グ�܂��B

=======================================================================

>> �]�k

 ���낻�� imgctl ����͎�������āA�\�[�X�R�[�h����V�������C�u������
 �쐬�������Ƃ���ł��B

 �c�Ə����Ă��瑁��N�B

=======================================================================

>> �X�V���� ('*'�������قǏd�v�ȍX�V�ł�)

> Version 1.00B [2001/12/08]
  **: HRK����̃z�[���y�[�W(http://www.meteo.ee.vu/)�ɂ��铮��e�X�g
      �f���ɂĉ����J����(�֐������t�@�C������^_^;)�B

> Version 1.00 [2001/12/18]
 ***: ���������[�X�B
 ***: HeadDIB, ColorDIB, DIBto16Bit �̂R�֐���ǉ��B
 ***: DIBto24Bit, DIBtoRLE, RLEtoDIB �̂R�֐��̎d�l��ύX�B
  **: SizeDIB �֐����폜�B

> Version 1.01B [2002/02/03]
 ***: ToDIB, PaletteDIB, PixelDIB, CutDIB, DIBtoPNGex �̂T�֐���ǉ��B
 ***: HeadDIB �֐��̃o�O���C���B

> Version 1.01B2 [2002/02/04]
 ***: ImgctlBeta, DCtoDIB �̂Q�֐���ǉ��B

> Version 1.01 [2002/02/06]
   *: DIBtoPNGex �֐��̓����d�l������ɕύX�B
  **: imgctl_util.c �� DIBtoPNGex �֐��̐�����ǉ��B

> Version 1.02B [2002/02/13]
 ***: DIBto8Bit �֐���ǉ��B
 ***: DIBto24Bit, DIBto16Bit �̂Q�֐��̃o�O���C���B

> Version 1.02B2 [2002/02/13]
 ***: GrayDIB, ToneDIB, ReplaceDIB �̂R�֐���ǉ��B

> [2002/02/19]
 ***: Borland Delphi 6 �ɑΉ������B
   *: imgctl.bas �Ƀo�[�W�������萔�ǉ��B

> Version 1.02 [2002/03/06]
  **: PNGtoDIB �֐��̕s�����C���B

> Version 1.03B [2002/03/16]
 ***: GetImageType, DIBto8Bit, BMPtoDIB �̂R�֐����g���B

> Version 1.03B2 [2002/03/17]
 ***: JPGtoDIB �֐����g���B

> Version 1.03B3 [2002/04/02]
 ***: GetImageType �֐����C���B

> Version 1.03 [2002/04/30]
  **: GetImageType �֐���PCX�`���̔��ʂ�ǉ��B

> Version 1.04B [2002/05/25]
 ***: GetImageType �֐����C���B

> Version 1.04 [2002/08/04]
 ***: DIBStretchDIBits2 �֐���ǉ��B

> Version 1.05B [2002/09/08]
 ***: PasteDIB �֐���ǉ��B
 ***: CutDIB �֐��̍������}�C�i�X���ɐ؂���͈͂��قȂ�s�����C���B
 ***: DIBDIBits, DIBStretchDIBits, DIBStretchDIBits2 �̂R�֐��̓]������
      �؂���͈͂��قȂ�s���C���B

> Version 1.05 [2002/09/23]
 ***: InfoPNG �֐���ǉ��B

> Version 1.06B [2002/10/10]
 ***: TurnDIB �֐���ǉ��B
   *: CutDIB �֐�����C���B
  **: �قȂ�o�[�W�����Ԃł̌݊�����������(v1.05�ȍ~)�B

> Version 1.06 [2002/11/12]
 ***: RepaintDIB �֐���ǉ��B
   *: �w�b�_�t�@�C�����ł̃^�C�v�~�X�A�X�y���~�X���C���B

> Version 1.07B [2002/11/25]
  **: GetImageType �֐���JPEG�`���̔��ʂ���C���B
  **: DIBDIBits, DIBStretchDIBits, DIBStretchDIBits2 �̂R�֐��̍��W��
      �����␳���폜(���API�֐��ɋ߂�����)�B

> Version 1.07B2 [2003/01/23]
 ***: ImgctlError, ImgctlErrorClear �̂Q�֐���ǉ��B
 ***: PixelDIB �֐��́ARLE-DIB���ƐF���擾�o���Ȃ��o�O���C���B
  **: GetDIB �֐��̏������C��(imgctl.txt�Q��)�B

> [2003/01/23]
  **: Visual C++ .net �ɑΉ������B
  **: Visual C++ .net �ŃR���p�C������(���s���x����)�B

> Version 1.07B3 [2003/01/26]
 ***: ImgctlError �֐��̃G���[�R�[�h��ǉ��B
 ***: HDIB�^�������Ɏ��֐���NULL�`�F�b�N������ǉ��B
  **: �t�@�C�����������Ɏ��֐���NULL�`�F�b�N������ǉ��B
 ***: �e�֐��̈����ɂ�����s����NULL�̃`�F�b�N������ǉ��B
 ***: Visual C# .net �ɂƂ肠�����Ή������B

> Version 1.07 [2003/02/10]
  **: JPEG���C�u�����y��PNG���C�u�������č\�z�����B

> Version 1.08B [2003/03/10] (v1.08�Ɍ�ݒ�)
  **: PointerOf �֐���ǉ��B(Visual Basic �����̊֐��ł�)
   *: �o�[�W����������萔 IMGCTL_VERSION_STRING ��ǉ��B
  **: imgctl.bas �� BITMAPINFO �f�[�^�^���C���B
  **: imgctl_util.bas �� DIBtoPNGex �֐��̐�����ǉ��B
  **: C++ �p�N���X ccImage ���L�q���ꂽ imgctl_class.h ��ǉ��B

> Version 1.08B2 [2003/03/10]
 ***: DataDIB, DIBtoDC, DIBtoDCex, DIBtoDCex2 �̂S�֐���ǉ��B
 ***: �������̊m�ە��@�� malloc ���� GlobalAlloc �ɕύX�B
 ***: DIB�f�[�^�i�[���@�ɂ��Ă̐����t�@�C�� dibdata.txt �ǉ��B
  **: imgctl_class.h �𐳎��ǉ�(�O�o�[�W�����͌�ݒ�L��)�B
  **: imgctl.pas �̍\���~�X���C��(��)�B

> Version 1.08 [2003/03/10]
 ***: DataDIB �֐��d�l�ύX�B
 ***: �������̊m�ە��@�� GlobalAlloc ���� malloc �ɖ߂���(��)�B

> Version 1.09 [2003/03/15]
 ***: DIBtoDC, DIBtoDCex �̂Q�֐��̎d�l��啝�C���B
      �����̊֐�������ŗ��p����ȉ��̊֐��ɂ��e�����܂��B
      DIBtoDCex2, DIBDIBits, DIBStretchDIBis, DIBStretchDIBits2
  **: ��̏C���ɔ����AImgctlError �֐��̃G���[�R�[�h��ǉ��B
  **: DIBtoPNGex �֐��ł̓��ߐF�w��̃o�O�C���B

> Version 1.10B [2003/03/20]
 ***: DIBtoDC, DIBtoDCex �̂Q�֐��̎d�l���C���B
      �����̊֐�������ŗ��p����ȉ��̊֐��ɂ��e�����܂��B
      DIBtoDCex2, DIBDIBits, DIBStretchDIBis, DIBStretchDIBits2
 ***: PasteDIB �֐��̃o�O�Ǝd�l���C���A�y�ы@�\�g���B
  **: ��̏C���ɔ����AImgctlError �֐��̃G���[�R�[�h��ǉ��B
  **: pasteproc.c, pasteproc.bas �̃T���v���֐��ǉ��B

> Version 1.10B2 [2003/03/25]
  **: GetImageType �֐��ŁAPIC�`����PICT�`�����������Ă���(��)�B
      �萔���AIMG_PICT �y�� IMG_PCT ���R�����g�A�E�g�B

> Version 1.10B3 [2003/03/25]
  **: DIBtoJPG, JPGtoDIB, DIBtoPNG, DIBtoPNGex �̂S�֐����g���B
   *: PNGtoDIB, InfoPNG �̂Q�֐����C���B

> Version 1.10B4 [2003/03/26]
 ***: DIBto16BitEx �֐���ǉ��B
 ***: GetImageType, CreateDIB, DIBto8Bit �̂R�֐����g���B
   *: DIBto16Bit, BMPtoDIB �̂Q�֐�����C���B
  **: 16Bit, 32Bit �̐F�ϊ��������C���B

> Version 1.10B5 [2003/03/27]
  **: DIBto16BitEx, DIBto8Bit �̂Q�֐����g���B

> Version 1.10B6 [2003/03/27]
 ***: DIBto16BitEx, DIBto8Bit �̂Q�֐����C���y�ъg���B

> Version 1.10B7 [2003/03/27]
 ***: DIBto16BitEx, DIBto8Bit �̂Q�֐����d�l�ύX�A�C���A�y�ъg���B

> Version 1.10B8 [2003/03/28]
   *: DIBto16BitEx, DIBto8Bit �̂Q�֐����g���B

> Version 1.10 [2003/03/29]
   *: DIBto16BitEx, DIBto8Bit �̂Q�֐����d�l�ύX�B

> Version 1.11B [2003/03/30]
   *: DeleteDIB �֐�����C���B
  **: �������p�� libpng.lib �y�� zlib.lib ���o�[�W�����A�b�v�B

> Version 1.11 [2003/04/02]
 ***: DIBtoJPG �֐����K�����s����Ƃ����v���I�o�O�C���B
  **: imgctl_util.bas �̍\���ԈႢ���C���B

> Version 1.12B [2003/04/06]
 ***: ResizeDIB �֐���ǉ��B
  **: InfoPNG �֐��̃p���b�g�擾�����̃o�O�C���B

> Version 1.12B2 [2003/04/06]
 ***: GammaDIB, ContrastDIB �̂Q�֐���ǉ��B
 ***: ResizeDIB �֐��̊g�又�������P�B

> Version 1.12B3 [2003/04/07]
 ***: TableDIB, ShadeDIB �̂Q�֐���ǉ��B
 ***: GammaDIB, ContrastDIB �̂Q�֐����d�l�ύX�B
  **: CreateDIB �֐����g���A�y�ѓ����d�l�ύX�B
   *: ToneDIB �֐��̓����d�l�ύX�B
  **: ImgctlError �֐��̃G���[�R�[�h��ǉ��B

> Version 1.12B4 [2003/04/15]
 ***: TurnDIBex �֐���ǉ��B

> Version 1.12B4f [2003/04/21]
  **: DataDIB �֐����C��(C/C++�̂�)�B
  **: ��ɔ����AIMGDATA �\���̃����o��const�w������O(C/C++�̂�)�B

> Version 1.12B4f2 [2003/05/07]
 ***: RepaintDIB ��DLL�Ăяo�����C��(VB�̂�)�B

> Version 1.12B5 [2003/05/18]
 ***: PNGAtoDIB �֐���ǉ��B
  **: PNGtoDIB �֐��̓����d�l�ύX�B
  **: ImgctlError �֐��̃G���[�R�[�h��ǉ��B
  **: pasteproc.c �̃T���v���֐��ǉ��B

> Version 1.12B6 [2003/06/11]
  **: DIBtoPNGex �֐��̓��ߏ������C���B

> Version 1.12B7 [2003/06/12]
 ***: DIBtoPNGex �֐��̓��ߏ������C���B
  **: �\���̂ɃA���C�������g���w��B
  **: PNGOPT �\���̂ɃA���C�������g�p�_�~�[�ϐ��ǉ��B

> Version 1.12B8 [2003/06/21]
 ***: DIBtoJPG �֐��Ŏ��s���Ƀt�@�C���N���[�Y����Ȃ��o�O���C���B
 ***: JPGtoDIB �֐��Ŏ��s���Ƀt�@�C���N���[�Y����Ȃ��o�O���C���B
   *: imgctl.bas �̃o�[�W�����萔���Â������~�X���C���B

> Version 1.12B9 [2003/07/15]
 ***: GetImageType �֐��̎d�l�ύX�B
  **: imgctl.cs �y�� imgctl.bas �̎蒼���B

> Version 1.12B10 [2003/09/07]
  **: GetImageType �֐���JPEG�`���̔��ʂ���C���B

> Version 1.12 [2003/11/26]
   *: DIBtoBMP �֐��̕s�v�c�ȏ������폜�B

> [2003/12/02]
  **: imgctl.bas �̕��@�~�X���C���B

> Version 1.13B [2003/12/12]
  **: JPGtoDIB �֐���CMYK�F��Ԃ�JPEG��ǂݍ��߂�悤�ɂȂ����B

> Version 1.13B2 [2003/12/18]
  **: �����I�� DIBtoJPG �֐��̓����d�l��ύX�B(imgctl.txt�Q��)

> Version 1.13B3 [2004/04/20]
   *: JPGtoDIB �֐��ŉ𑜓x���ςȒl�ɐݒ肳��邱�Ƃ�����̂��C���B

> Version 1.13B4 [2004/06/21]
 ***: DIBtoGIF, DIBtoGIFex, GIFtoDIB, GIFtoDIBex �̂S�֐���ǉ��B
   *: C#����ւ̑Ή����~�߁Aimgctl.cs ��P���B
   *: C++�N���X imgctl_class.h ��P���B

> Version 1.13 [2004/06/23]
 ***: DIBtoGIFAni, DIBtoGIFAniEx �̂Q�֐���ǉ��B

> Version 1.14 [2004/07/03]
 ***: GIFtoDIB, GIFtoDIBex �̂Q�֐��̒v���I�ȃo�O���C���B

> [2004/07/04]
   *: �T���v���������������������B

> Version 1.15 [2004/08/24]
 ***: DIBto24Bit �֐���32�r�b�gDIB������ɕϊ��ł��Ȃ��o�O���C���B
  **: �����I�� DIBto8Bit �֐��̓����d�l��ύX�B(imgctl.txt�Q��)

> Version 1.16B [2004/08/30]
  **: �������p�� libpng.lib �y�� zlib.lib ���o�[�W�����A�b�v�B

> Version 1.16B2 [2004/09/11]
 ***: PNG�摜������ɍ쐬����Ȃ��Ȃ��Ă����o�O���C���B
   *: �������p�� libpng.lib ���o�[�W�����A�b�v�B

> [2004/09/30]
 ***: imgctl.pas �̕��@�~�X���C���B

> Version 1.16B3 [2005/01/18]
 ***: BMPMtoDIB, JPGMtoDIB, PNGMtoDIB, PNGMAtoDIB, InfoPNGM,
      GIFMtoDIB, GIFMtoDIBex �̂V�֐���ǉ��B
  **: ImgctlError �֐��̃G���[�R�[�h��ǉ��B

> Version 1.16B4 [2005/01/28]
 ***: �������p�� libpng.lib �Ƀ��`�����l���t��PNG��ǂݍ��߂Ȃ��o�O��
      ���������߁A�ŐV�łɃo�[�W�����A�b�v�B

> Version 1.16B5 [2005/02/01]
 ***: GIF�����o���n�֐��ŕs���� 0 �������o�����Ƃ��������o�O���C���B

> Version 1.16 [2005/02/01]
 ***: GetImageMType, MtoDIB �̂Q�֐���ǉ��B
  **: GetImageType �֐��̓����d�l��ύX�B

> Version 1.17 [2005/02/03]
 ***: GIF�ǂݍ��݌n�֐��̃o�O���C���B

> Version 1.18 [2005/04/20]
 ***: BMPtoDIB �֐����C���B
 ***: TurnDIB �֐���1,4�r�b�gDIB��]���ɗ��ꂪ������o�O���C���B

> Version 1.19 [2005/06/14]
 ***: PNGtoDIB, PNGMtoDIB �̂Q�֐���2�r�b�gPNG�ǂݍ��݃o�O���C���B

> Version 1.20 [2005/07/26]
 ***: DIBtoGIFex, DIBtoGIFAniEx �̂Q�֐��̓��ߐF�Ɋւ���o�O���C���B

> Version 1.21 [2006/02/04]
 ***: BMPtoDIB, BMPMtoDIB �̂Q�֐��̃r�b�g�t�B�[���hBMP���ǂݍ��߂Ȃ�
      �o�O���C���B
 ***: DIBtoRLE �֐��ł��܂�RLE�ϊ�����Ȃ����Ƃ��������o�O���C���B
 ***: CutDIB �֐��Ńr�b�g�t�B�[���hBMP�̃^�C�v�������������Ă��܂�
      �o�O���C���B
   *: imgctl.txt �̕\�L�~�X���C���B

> Version 1.22 [2006/02/05]
 ***: BMPtoDIB, BMPMtoDIB �̂Q�֐��̃r�b�g�t�B�[���hBMP���ǂݍ��߂Ȃ�
      �o�O�����x�����C���B

> Version 1.23 [2006/03/26]
  **: ResizeDIB �֐��̊g�又���̓����d�l��ύX�B

> Version 1.24 [2007/02/27]
  **: �������p��JPEG���C�u������IJG�W���� libjpeg ����
      IJG's JPEG software with x86 SIMD extension �ɕύX�B
   *: �������p�� libpng �y�� zlib ���o�[�W�����A�b�v�B

> Version 1.25 [2009/02/19]
 ***: �s����JPEG�ǂݍ��݂Ńt���[�Y����o�O���C���B
 ***: GIF�ǂݍ��݂Ńt���[�Y����\��������o�O�̏C���B
 ***: �[�����Z���N������֐����C���B
  **: GetImageType �֐���V4,V5�^�C�v��BMP��F���ł���悤�ɏC���B
   *: JPEG���C�u�����̃R�[�h�팸���K�p�����B
   *: �������p�� libpng ���o�[�W�����A�b�v�B
   *: �r���h���� Visual Studio 2005 �ɕύX(�c�̉e�����T�C�Y����)�B

> Version 1.26 [2009/04/06]
 ***: RGB�`����JPEG��ǂݍ��ނ�R��B�����]���Ă��܂��o�O���C���B
  **: Adobe Photoshop ��CMYK�`���ŕۑ�����JPEG�̓ǂݍ��݂ɉ��Ή��B
  **: �s����GIF�摜��ǂݍ��ނƃt���[�Y����ꍇ������o�O���C���B

> Version 1.27 [2010/03/06]
 ***: �������p�� libpng ���o�[�W�����A�b�v(�Ǝ㐫�΍�̈�)�B

=======================================================================

>> �A����

 ���[�`�F's Homepage [��҃T�C�g]
     http://www.ruche-home.net/

 ���[���A�h���X [�T�|�[�g�p]
     info@ruche-home.net

=======================================================================
README  2010-03-06  by ruche.