# maya_rotationDriver
�{�[���̃I�C���[�p��]���A�{�[�����������ɂ����u�P��^�c�����̋Ȃ��^�������̋Ȃ��v�Ƃ����Ɨ������O�̊p�x�ɕ����E��������Maya�v���O�C����Python�����̊ȒP�ȃT���v���ł��B

##�f�B���N�g���\��
* scripts: �A�g���r���[�g�G�f�B�^���C�A�E�g��`�p��mel�X�N���v�g�B
* plug-ins: Python�ɂ��v���O�C���B
* examples: �����ȒP��Maya 2016�V�[���̗�B

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
decomposeRotate �m�[�h�� composeRotate �m�[�h�̐ݒ肪���S�ɓ����ł���΁A�����������̂��������Č��ɖ߂����Ƃ��o���܂��B
