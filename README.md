# Скрипт для конретации модели в формат model.plan

Запуск происходит через команду в корне 
```code
ansible-playbook -i inventory.ini playbook.yml \
    # Тут можно прописать, на какой киоск мы хотим прокидывать (убрать строчку, если сразу на оба)
    -l kiosk2 \ 

    # Путь до папки models, где лежат все модели из репы (например models/plai_object_models)
    -e "model_src_dir=".models"

    # Путь до папки, где уже лежат нужная модель, например:
    -e "model_subdir=plai_object_models/yolov8/20250919_padel_player_new_court_on_hard_examples_8s_e100_bs16_s640" 
   
```

