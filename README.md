# maya_rotationDriver
�{�[���̃I�C���[�p��]���A�{�[�����������ɂ����u�P��^�c�����̋Ȃ��^�������̋Ȃ��v�Ƃ����Ɨ������O�̊p�x�ɕ����E��������Maya�v���O�C����Python�����̊ȒP�ȃT���v���ł��B

##���̎�@�ɂ���
���̎�@��p����ƁA�֐߂��ǂ̕����ɂǂꂭ�炢�Ȃ��������P��ꂽ���ɂ���āA�ʂ̉������쓮�����邱�Ƃ��I�m�ɏo���܂��B�����A�I�C���[�p��]��p���Ă������낤�Ƃ���ƈȉ��̂悤�ȏ�Q������܂��B

* ��̎p����\���l�̑g�ݍ��킹�������ɑ��݂���i���̎�@�ł͈�����L�蓾�Ȃ��j�B
* �X�̎���]���P���Ȃ���\���킯�ł͂Ȃ��iX�������ɐL�т����̔P�肪�I�C���[�p��X����]�Ƃ͌���Ȃ��j�B

�I�C���[�p��]�̃f�����b�g�����̂܂܂��̎�@�̃����b�g�ł��B
���̎�@�ł́A�����̃m�[�h�Ƌ��ɍ����̃m�[�h������A���������l���󂯂ăh���u���L�[���Ńt�B���^������ōč������ĕʂ̍����쓮�����邱�Ƃ��o���܂��i�Ⴆ�΁A�Ȃ���50%�����Ǐ]������Ȃǁj�B

##�f�B���N�g���\��
* scripts: �A�g���r���[�g�G�f�B�^���C�A�E�g��`�p��mel�X�N���v�g�B
* plug-ins: Python�ɂ��v���O�C���B
* examples: �����ȒP��Maya�V�[���̗�ƁA�O�Ղ��v���b�g����T���v���X�N���v�g�B

##�m�[�h�ɂ���
�v���O�C�� rotationDriver.py �͈ȉ��̓�̃m�[�h���܂�ł��܂��B

* decomposeRotate
  �I�C���[�p��]����͂��āu�P��^�c�����̋Ȃ��^�������̋Ȃ��v���o�͂���m�[�h�B
  �ȉ��̃A�g���r���[�g�������܂��B
  - method: ������@�̑I���B
  - reverseOrder: OFF���ƋȂ��E�P��̏��AON���ƔP��E�Ȃ��̏��ɂȂ�悤�ɕ�������i���ʂ�����̂� method �� Stereographic Projection �̏ꍇ�̂݁j�B
  - rotate: �I�C���[�p��]�̓��́B
  - rotateOrder: ���͉�]�̃I�[�_�[�B
  - axisOrient: �{�[���������`���邽�߂̉�]�B
  - outDecomposedAngle: �������ꂽ�O�̊p�x�̏o�́B

* composeRotate
  �u�P��^�c�����̋Ȃ��^�������̋Ȃ��v����͂��ăI�C���[�p��]���o�͂���m�[�h�B
  �ȉ��̃A�g���r���[�g�������܂��B
  - method: ������@�̑I���B
  - reverseOrder: OFF���ƋȂ��E�P��̏��AON���ƔP��E�Ȃ��̏��ɂȂ�悤�ɍ�������i���ʂ�����̂� method �� Stereographic Projection �̏ꍇ�̂݁j�B
  - decomposedAngle: �������ꂽ�O�̊p�x�̓��́B
  - axisOrient: �{�[���������`���邽�߂̉�]�B
  - rotateOrder: �o�͉�]�̃I�[�_�[�w��B
  - outRotate: �������ꂽ�I�C���[�p��]�̏o�́B

##�p�x�̕����E������@�̑I��
method �A�g���r���[�g�ɂ���āA�p�x�̕����E������@���A
[Stereographic Projection](https://ja.wikipedia.org/wiki/%E3%82%B9%E3%83%86%E3%83%AC%E3%82%AA%E6%8A%95%E5%BD%B1)
�� Exponential Map �̂ǂ��炩��I�����邱�Ƃ��o���܂��B

Stereographic Projection �ł̕����́A�܂����͉�]���Ȃ��ƔP��ɕ���������ɁA�Ȃ���]���ˉe�ɂ���ďc�������ɕ������܂��B�����ł͂��̋t�����܂��B�c���̋Ȃ��ɂ͉�]�̏��Ԃ͂���܂��񂪁A�Ȃ��ƔP��ɂ͏��Ԃ�����܂��BreverseOrder �� OFF �̏ꍇ�͊K�w��ʂ��猩�ċȂ��E�P��̏��AON �̏ꍇ�͔P��E�Ȃ��̏��ƂȂ�܂��B

Exponential Map �ł̕����̓N�H�[�^�j�I���� log() �̂Q�{�A�����͓��͂�1/2�{�� exp() �Ƃ��Ă��܂��BMaya API �� MQuaternion �N���X�ɂ͂����̃��\�b�h������̂ŁA�������Ăяo�������̔��ɊȒP�Ȏ����ƂȂ��Ă��܂��BStereographic Projection �ɋ߂��l���Z�o����܂����A������͋Ȃ��E�P��̏��Ԃ�����܂���B

�\�[�X�R�[�h������Ε�����܂����A���� method ���ǂ���̏ꍇ�ɂ� reverseOrder �� ON �̏ꍇ�͔��]�������s���Ă��܂��B�����[�����ƂɁAExponential Map �̏ꍇ�͂��̈Ⴂ������܂���B

�T���v���X�N���v�g [examples/plotBendHV.py](https://github.com/ryusas/maya_rotationDriver/tree/master/examples/plotBendHV.py) �� Maya ��Ŏ��s����ƁA�c�����Ɖ������̋Ȃ���ω����������ɕ`����鋅�ʏ�̋O�Ղ��v���b�g����܂��B����œ��ނ̋Ȃ���]�̌��ʂ̈Ⴂ���m�F�o���܂��B

![SS](/plotBendHV.png)

�����ȋȂ���]�Ƃ����_�ł� Stereographic Projection �̕����Y��ȃv���b�g���ʂ������܂��BStereographic Projection �ł� 180�x�̋Ȃ��͂��傤�ǔ��Α��̋ɂɎ������܂����AExponential Map �ł͋ɂ��I�[�o�[���Đ����������Ă��܂��܂��B

��]���Ȃ��ƔP��ɕ������Ĉ����Ƃ����l���ł� Stereographic Projection ���K���Ă��āA
�Ȃ��ƔP��̏��Ԃ������������Ĉ����ɂ� Exponential Map ���K���Ă���Ƃ�����̂ł͂Ȃ����Ǝv���܂��B

##�{�[���������̒�`
�f�t�H���g�ł́A���[�J��X�����{�[�������AY�����c�����AZ�����������ƂȂ��Ă��āA����Ɋ�Â��������E����������܂��B
axisOrient �A�g���r���[�g�ɂ���āA���̕�������]�����邱�Ƃ��o���܂��B
decomposeRotate �m�[�h�� composeRotate �m�[�h�̐ݒ肪�����ł���΁A�����������̂��������Č��ɖ߂����Ƃ��o���܂��B

##�T���v���V�[��
* [examples/rotationDriver.ma](https://github.com/ryusas/maya_rotationDriver/tree/master/examples/rotationDriver.ma)

  ��̃L���[�u pCube1 �̉�]����������̃L���[�u pCube2 �̉�]�����̂܂܋쓮�����B
  pCube1 �̉�]�� decomposeRotate �ŕ������A�������ꂽ�R��]�� pCube2 �̓��͂ƂȂ��Ă��� composeRotate �ɂ��̂܂܌q���Ă��܂��B
  �o�����S�������p���ɂȂ�̂��m�F�o���܂��BdecomposeRotate �� composeRotate �� method �� reverseOrder ���̐ݒ���������Ă݂�ƕ�����܂����A�o�����S�������ݒ�ɂȂ��Ă���K�v������܂��B

* [examples/rotationDriver_joints.ma](https://github.com/ryusas/maya_rotationDriver/tree/master/examples/rotationDriver_joints.ma)

  ��̃{�[�� src �̉�]����������̃{�[�� dst �̉�]�����̂܂܋쓮�����B
  �L���[�u�̗�Ɠ����ł����A�{�[���̃��[�J���������������ĕς��Ă���AcomposeRotate �� axisOrient �A�g���r���[�g�ɂ���ĕ�������v�����Ă��܂��B

* [examples/bend_roll.ma](https://github.com/ryusas/maya_rotationDriver/tree/master/examples/bend_roll.ma)
  �Ȃ��ƔP��ɕ���������]���A�Ȃ��ƔP��̏��Ԃ��قȂ��̊K�w�ɕ����Đڑ����Ă����B
  reverseOrder ��ς��邽�߂� decomposeRotate �m�[�h������ē��ނ̕������ʂ𓾂Ă��܂��B������Ȃ��ƔP��̏������قȂ��� joint �K�w�ɐڑ����Ă��܂��B
  ���ꂼ��� reverseOrder �̐ݒ肪�K�؂łȂ��Ɗ��҂��錋�ʂ͓����܂���B
  �܂� method �� Stereographic Projection �ł����AExponential Map �ɂ���Ɗ��҂��錋�ʂ͓����܂���B

##��������
* 2016.9.20: reverseOrder�A�g���r���[�g�ǉ��A�T���v���V�[���ǉ��ƃh�L�������g���M�B
* 2016.7.9: ����
