# The-Simpsons-Characters-Classification
Решение задачи классификации на прмере [датасета Симпсонов](https://www.kaggle.com/datasets/alexattia/the-simpsons-characters-dataset).

В качестве архиетуктуры выступает модифицированный VGG с Адаптивным пулингом.

*simpsons915.ipynb* - лучшее решение, значение метрики *F1 = 91.5%*.

Оптимизатор *Adam*  с параметрами по умолчанию, scheduler, аугментации *RandomHorizontalFlip + RandomRotation(5)*, L2-регуляризация. 

В папке *aug test* приведены разные аугментации.

Сравнение аугментаций (F1 Score):

без аугментаций - 90.6%

RandomHorizontalFlip - 91.26%

RandomVerticalFlip - 88%

RandomHorizontalFlip + RandomVerticalFlip - 86.51%

RandomHorizontalFlip + RandomRotation(5) - 91.5% !!!

RandomHorizontalFlip + RandomRotation(10) - 90.78%

RandomHorizontalFlip + ColorJitter(brightness=0.1, contrast=0.1) - 87.5%

В папке *runs-l1-l2* приведены версии с L1 и L2 регуляризацией + гистограммы весов TensorBoard.

*simpsons915 adamw.ipynb* - версия с оптимизатором AdamW (работает хуже).
