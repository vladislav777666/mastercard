# mastercard
for DECENTRATHON3.0

# Инструкция по воспроизведению эксперимента в Google Colab

## Описание
мы используем GMM по следующим причинам:
Гибкость формы кластеров:
GMM допускает кластеры эллиптической формы с разной дисперсией, что лучше подходит для транзакционных данных, где клиенты могут иметь сложные распределения.
(\( k=7 \)) на основе транзакционных данных из `DECENTRATHON_3.0.parquet`.

## Требования
- Google Colab (Python 3.8+).
- Зависимости (указаны в `requirements.txt`):
pandas==2.2.2
numpy==1.26.4
scikit-learn==1.5.1
matplotlib==3.9.2
seaborn==0.13.2
joblib==1.4.2
onnx==1.16.2
skl2onnx==1.16.0
faker==28.1.0
pyarrow==17.0.0
- Датасет: `DECENTRATHON_3.0.parquet`.

## Запуск
1. Откройте `segmentation.ipynb`
2. Вставьте `DECENTRATHON_3.0.parquet`
3. В ячейку введите `!pip install -r /content/requirements.txt --force-reinstall`
5. Выполняйте ячейки последовательно (Shift+Enter).
6. Проверьте путь к файлу данных в ячейке загрузки.

## Выходные файлы
- `/data_dictionary.csv`: Описание полей и метрик.
- `/segmented.parquet`: Результаты сегментации (`card_id`, сегмент, описание).
- `/segment_stats.csv`: Статистика по сегментам.
- `/metrics.csv`: Вычисленные метрики.
- `/client_segmentation.onnx`: Модель GMM в формате ONNX.
- `/scaler.pkl`: Стандартизатор.
- `/elbow_plot.png`, `/silhouette_plot.png`, `/segment_visualization.png`: Визуализации.
- `/segmentation.log`: Логи выполнения.
- Скачайте файлы из раздела "Files" в Colab.


## Контакты
Для вопросов: обратитесь к разработчику проекта.
telegram @geniys666