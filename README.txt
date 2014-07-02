jquery.jpostal.js
=================

�X�֔ԍ�����͂���ƏZ�����֎������͂���jQuery�v���O�C���ł��B

--------------------------------------------------
�g�p��
--------------------------------------------------
(sample_1.html)

<script type="text/javascript" src="//code.jquery.com/jquery-2.1.0.min.js"></script>
<script type="text/javascript" src="jquery.jpostal.js"></script>
<script type="text/javascript">
$(window).ready( function() {
	$('#postcode1').jpostal({
		postcode : [
			'#postcode1',
			'#postcode2'
		],
		address : {
			'#address1'  : '%3',
			'#address2'  : '%4',
			'#address3'  : '%5'
		},
		url : {
			'http'  : 'json/',
			'https' : 'json/',
		},
	});
});

--------------------------------------------------
�ݒu���@
--------------------------------------------------
1. jquery.jpostal.js���T�[�o�ɐݒu���Ă��������B

  �A�b�v���[�h��͔C�ӂł��B
  html�t�H�[���ƈႤ�T�[�o���\�ł��B
  �A�b�v���[�h��̗�1  js/jpostal/jquery.jpostal.js
  �A�b�v���[�h��̗�2  js/jquery.jpostal.js
  
2. json/*.json ���T�[�o�ɃA�b�v���[�h���Ă��������B

  �A�b�v���[�h��͔C�ӂł��B
  jquery.jpostal.js�Ƃ̑��Ί֌W�͂���܂���B
  html�t�H�[���Ajquery.jpostal.js�ƈႤ�T�[�o�ł����܂��܂���B
  �A�b�v���[�h��̗�1  js/jpostal/json/*.json
  �A�b�v���[�h��̗�2  js/json/*.json

3. �Z�����̓t�H�[����jquery�{�̂�jquery.jpostal.js���C���N���[�h���Ă��������B

  ��
  <script type="text/javascript" src="//code.jquery.com/jquery-2.1.0.min.js"></script>
  <script type="text/javascript" src="js/jquery.jpostal.js"></script>

4. jpostal�v���O�C���Ăяo�����L�q���Ă��������B

4-1. .jpostal���w�肷��Z���N�^

$('#postcode1').jpostal({

	�X�֔ԍ����̃Z���N�^���w�肵�Ă��������B
	�X�֔ԍ�����2�̏ꍇ�́A�ŏ���1�������w�肵�Ă��������B
	DOM id��ݒ肵�Ă����ق����w�肪�ȒP�ł��B

	��1
	<input id="postcode1_1" name="postcode1" />
	$('#postcode1_1').jpostal({

	��2
	DOM id�Ȃ��̏ꍇ
	<input name="postcode1" />
	$('[name=postcode1]').jpostal({

4-2. ����

postcode	�X�֔ԍ���
	�X�֔ԍ����Z���N�^�̔z��
	
	��1
	�X�֔ԍ�����1��
	postcode : [
		'#postcode'
	]

	��2
	�X�֔ԍ�����2��
	postcode : [
		'#postcode1',
		'#postcode2'
	]
			
address		�Z����
	�Z�����Z���N�^�Ɠ��͍��ڃt�H�[�}�b�g�̘A�z�z��

	���͍��ڃt�H�[�}�b�g
	%3	�s���{��
	%4	�s�撬��
	%5	����
	%6	������Ə��̔Ԓn
	%7	������Ə��̖���
	
	��1
	�s���{�����A�Z������2��
	address : {
		'#prefecture'  : '%3',
		'#address'     : '%4%5',
	}

	��2
	�s���{�����A�Z�����A�Ԓn����3��
	address : {
		'#prefecture'  : '%3',
		'#address1'    : '%4',
		'#address2'    : '%5',
	}

url		json/*.json��URL
	�Z���t�H�[������json/*.json�ւ̑���URL�܂��͐��URL�B
	http�p�Ahttps�p���w�肵�Ă��������B

	��1
	url : {
		'http'  : 'json/',
		'https' : 'json/'
	}

	��2
	url : {
		'http'  : 'http://www.example.jp/json/',
		'https' : 'https://ssl.example.jp/mysite/json/'
	}

	��3
	http�Ahttps �ǂ���������z�X�g�ƃp�X�̏ꍇ
	url : {
		'http'  : '//www.example.jp/json/',
		'https' : '//www.example.jp/json/'
	}
