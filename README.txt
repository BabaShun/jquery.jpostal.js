jquery.jpostal.js
=================

�X�֔ԍ�����͂���ƏZ�����֎������͂���jQuery�v���O�C���ł��B
ver2.0 beta �J����
ver2.1 �����[�X�\��


�g�p��
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
</script>
