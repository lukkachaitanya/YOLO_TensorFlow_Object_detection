# YOLO_tensorflow

(Version 0.3, Last updated :2017.02.21)

### 1.Introduction


### 2.Install

(2) Download YOLO weight file from

YOLO_small : https://drive.google.com/file/d/0B2JbaJSrWLpza08yS2FSUnV2dlE/view?usp=sharing


(3) Put the 'YOLO_(version).ckpt' in the 'weight' folder of downloaded code

### 3.Usage

(1) direct usage with default settings (display on console, show output image, no output file writing)

	python YOLO_(small or tiny)_tf.py -fromfile (input image filename)

(2) direct usage with custom settings

	python YOLO_(small or tiny)_tf.py argvs

	where argvs are

	-fromfile (input image filename) : input image file
	-disp_console (0 or 1) : whether display results on terminal or not
	-imshow (0 or 1) : whether display result image or not
	-tofile_img (output image filename) : output image file
	-tofile_txt (output txt filename) : output text file (contains class, x, y, w, h, probability)

(3) import on other scripts

	import YOLO_(small or tiny)_tf
	yolo = YOLO_(small or tiny)_tf.YOLO_TF()

	yolo.disp_console = (True or False, default = True)
	yolo.imshow = (True or False, default = True)
	yolo.tofile_img = (output image filename)
	yolo.tofile_txt = (output txt filename)
	yolo.filewrite_img = (True or False, default = False)
	yolo.filewrite_txt = (True of False, default = False)

	yolo.detect_from_file(filename)
	yolo.detect_from_cvmat(cvmat)

### 4.Requirements

- Tensorflow
- Opencv2


# YOLO_TensorFlow_Object_detection
