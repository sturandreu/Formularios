Formularios
===========

codigo para los formularios

con estas lineas se validan los campos del formulario
-----------------------------------------------------------------------
<?php $form=$this->beginWidget('bootstrap.widgets.TbActiveForm',array(
  'id'=>'products-category-form',
	'enableAjaxValidation'=>false,
	'type'=>'horizontal',
	'enableClientValidation'=>true,
	'clientOptions'=>array(
						'validateOnSubmit'=>true,
					),
)); ?>


con estas lineas colocamos los campos hidden del formulario, no se mostraran al usuario
----------------------------------------------------------------------------------------

<?php //echo $form->textFieldRow($model,'datecreate',array('class'=>'span5')); ?>

  <?php 	
			echo $form->hiddenField($model,'datemodify',array('class'=>'span5','value'=>date('Y-m-d H:m:s')));
		if ($model->isNewRecord) {
			echo $form->hiddenField($model,'usercreate',array('class'=>'span5','value'=>Yii::app()->user->id));
		}
	 echo $form->hiddenField($model,'usermodify',array('class'=>'span5','value'=>Yii::app()->user->id)); ?>

