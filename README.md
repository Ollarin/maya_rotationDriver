# maya_rotationDriver
�{�[���̃I�C���[�p��]���A�{�[�����������ɂ����u�P��^�c�����̋Ȃ��^�������̋Ȃ��v�Ƃ����Ɨ������O�̊p�x�ɕ����E��������Maya�v���O�C����Python�����̊ȒP�ȃT���v���ł��B

##�f�B���N�g���\��
* scripts: �A�g���r���[�g�G�f�B�^���C�A�E�g��`�p��mel�X�N���v�g�B
* plug-ins: Python�ɂ��v���O�C���B
* examples: �����ȒP��Maya 2016�V�[���̗�ƁA�O�Ղ��v���b�g����T���v���X�N���v�g�B

##�m�[�h�ɂ���
�v���O�C�� rotationDriver.py �͈ȉ��̓�̃m�[�h���܂�ł��܂��B

* decomposeRotate
  �I�C���[�p��]����͂��āu�P��^�c�����̋Ȃ��^�������̋Ȃ��v���o�͂���m�[�h�B
  �ȉ��̃A�g���r���[�g�������܂��B
  - method: ������@�̑I���B
  - rotate: �I�C���[�p��]�̓��́B
  - rotateOrder: ���͉�]�̃I�[�_�[�B
  - axisOrient: �{�[���������`���邽�߂̉�]�B
  - outDecomposedAngle: �������ꂽ�O�̊p�x�̏o�́B

* composeRotate
  �u�P��^�c�����̋Ȃ��^�������̋Ȃ��v����͂��ăI�C���[�p��]���o�͂���m�[�h�B
  �ȉ��̃A�g���r���[�g�������܂��B
  - method: ������@�̑I���B
  - decomposedAngle: �������ꂽ�O�̊p�x�̓��́B
  - axisOrient: �{�[���������`���邽�߂̉�]�B
  - rotateOrder: �o�͉�]�̃I�[�_�[�w��B
  - outRotate: �������ꂽ�I�C���[�p��]�̏o�́B

##�{�[���������̒�`�ɂ���
�f�t�H���g�ł́A���[�J��X�����{�[�������AY�����c�����AZ�����������ƂȂ��Ă��āA����Ɋ�Â��������E����������܂��B
axisOrient �A�g���r���[�g�ɂ���āA���̕�������]�����邱�Ƃ��o���܂��B
decomposeRotate �m�[�h�� composeRotate �m�[�h�̐ݒ肪�����ł���΁A�����������̂��������Č��ɖ߂����Ƃ��o���܂��B

[examples/rotationDriver_joints.ma](https://github.com/ryusas/maya_rotationDriver/tree/master/examples/rotationDriver_joints.ma) �́A���[�J�����̈قȂ��̃{�[���� axisOrient �ݒ���g���ē��������Ă����ł��B

##Exponential Map �ł̋ߎ��ɂ���
method �A�g���r���[�g�ɂ���āA�p�x�̕����E������@���A
[Stereographic Projection](https://ja.wikipedia.org/wiki/%E3%82%B9%E3%83%86%E3%83%AC%E3%82%AA%E6%8A%95%E5%BD%B1)
�� Exponential Map �̂ǂ��炩��I�����邱�Ƃ��o���܂��B

�\�[�X�R�[�h������Ε�����܂����AExponential Map �� Maya API �� MQuaternion ���N���X��p�������ɊȒP�Ȏ����ł��B
������ log() ���Q�{���ďo�́A�����͓��͂̔����� exp() ���Ă��邾���ł��B

�T���v���X�N���v�g [examples/plotBendHV.py](https://github.com/ryusas/maya_rotationDriver/tree/master/examples/plotBendHV.py) �� Maya ��Ŏ��s����ƁA�c�����Ɖ������̋Ȃ���ω����������ɕ`����鋅�ʏ�̋O�Ղ��v���b�g����܂��B����œ��ނ̌��ʂ̈Ⴂ���m�F�o���܂��B

![SS](/plotBendHV.png)
