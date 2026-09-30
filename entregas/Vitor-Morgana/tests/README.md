# Testes e validações

O projeto não possui uma suíte de testes automatizados versionada. As verificações reproduzíveis da entrega são:

```bash
cp .env.example .env
docker compose config --quiet
docker compose up --build
```

Após configurar `YOUTUBE_API_KEY` em `.env`, dispare a DAG `youtube_pipeline` no Airflow e confirme a conclusão de todas as tarefas. O pipeline valida datas, configurações de canais e termos de relevância; vídeos fora dos critérios ficam registrados em `data/silver/<run_id>/videos_descartados.parquet`.

Remova o `.env` local após a validação quando ele não for mais necessário. Os contratos, artefatos esperados e limitações estão documentados em [../docs/repository_context.md](../docs/repository_context.md).
