Projekt Inteligentny Śmietnik

Celem projektu jest nauczenie modelu, by na podstawie zdjęć odpadów klasyfikował je do jednej z 6 klas.
Model mógłby znaleźć zastosowanie w tzw. Inteligentnych Śmietnikach, które samodzielnie sortowałyby śmieci.

Główny kod znajduje się w pliku model.ipynb
Są tam przygotowane datasety oraz dataloadery, gotowy do użycia prosty klasyfikator CNN oraz ResNet18.
Następnie w kodzie są pętle do trenowania, testowania i walidacji, wizualizacja wyników uczenia modelu (ResNet) orz test dla przykłądowego obrazu

Dataset waży ~70MB i można go znaleźć pod linkiem: https://universe.roboflow.com/cybertech-qde01/waste-classification-q75av-awlnx

Poza plikiem z kodem w repozytorium znajdują się również następujące pliki:
- best_model.pth - zapisany model będący najlepszym checkpointem w trakcie treningu
- final_model.pth - zapisany po treningu najlepszy model
- training_history.png - wykresy błędu i dokładności dla setu treningowego i walidacyjnego

Kod był uruchamiany przez środowisko wirtualne utworzone w następujący sposób:

conda create --name namehere python=3.11

i aktywowane:

conda activate namehere

Konieczne jest również doinstalowanie bibliotek: 

pip install torch torchvision pillow tqdm

Najwyższy validation loss, jaki udało się osiągnąć wynosi 85.32%, wykresy błędu oraz dokładności wyglądają następująco:

<img width="1189" height="390" alt="image" src="https://github.com/user-attachments/assets/7ebfe270-2713-4901-a4a5-7a179f78a87f" />

Natomiast dla losowego obrazu z setu testowego wytrenowany model sklasyfikował go poprawnie z confidence: 91.96% 


