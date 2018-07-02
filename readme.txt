カメラで読み込んだ画像をGUIでパラメータ処理するプログラム.
フィルタは平坦化フィルタを用いている.
コントラストの変更はガンマ変換を用いている.
  GUIバー:
          fillter:画像全体にフィルタを適用.
          gam:画像全体のコントラストを変更.
          R:画像のR(red)要素のコントラストを変更.
          G:画像のG(green)要素のコントラストを変更.
          B:画像のB(brue)要素のコントラストを変更.

依存ライブラリ:
  拡張子はipynbより,jupyternotebookでの実行が望ましい.
  Python 3.6.5
  opencv-python 3.4.1.15
  numpy 1.14.5

使い方:
  fillterの大きさを上げるとフィルタの適用範囲が大きくなる(バー0の位置で範囲1(フィルタの適用なし),フィルタの範囲1~11).
  gam,R,G,Bの大きさを上げるとガンマ変換のガンマの値が大きくなる.
      (gam,R,G,Bそれぞれバー9の位置でガンマ1,バーが1進むごとにガンマ値+0.1 ガンマの範囲は0.1~10.1)

実行の様子:
  (URL:)https://youtu.be/OL8PpveMtZs

参考文献:
PythonとOpenCVで画像処理【トラックバー】 - 無能Fラン学生のお勉強おメモ
  ~【RGBで色を指定するトラックバーを生成】以下コード5~18行目
  (URL:)http://rasp.hateblo.jp/entry/2016/01/24/214027
で"cv2.createTrackbar"と"cv2.getTrackbarPos"の利用方法をpythonにおけるGUI処理の参考とした.

note.nkmk.me
Python, OpenCVでBGRとRGBを変換するcvtColor
 ~ 1行目: "OpenCVの関数imread()で画像ファイルを読み込むと色の順番がBGR（青、緑、赤）になる"
 より,画像の配列がBGRであることを確認.
  (URL:)https://note.nkmk.me/python-opencv-bgr-rgb-cvtcolor/
