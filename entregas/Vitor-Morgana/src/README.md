# Código-fonte

- `bronze_collect_videos.py` e `bronze_collect_comments.py`: ingestão da YouTube Data API v3.
- `silver_select_relevant_videos.py`, `silver_transform_videos.py` e `silver_transform_comments.py`: seleção de relevância, limpeza e padronização.
- `gold_add_sentiment.py`, `gold_create_aggregations.py`, `gold_create_temporal_series.py` e `gold_enrich_datasets.py`: enriquecimento Gold e artefatos analíticos.
- `silver/`: utilitários compartilhados de limpeza e relevância.

A execução é acionada pela DAG em `../dags/youtube_pipeline.py`. Consulte o [README principal](../README.md) para configuração e uso.
