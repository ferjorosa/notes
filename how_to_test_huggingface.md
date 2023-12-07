To run a test you need to run:
```
RUN_SLOW=1 pytest tests/models/flava/test_modeling_flava.py::FlavaForPreTrainingIntegrationTest
```

To debug a test, you need to update the `.vscode/launch.json` file:

```
{
    // Use IntelliSense para saber los atributos posibles.
    // Mantenga el puntero para ver las descripciones de los existentes atributos.
    // Para más información, visite: https://go.microsoft.com/fwlink/?linkid=830387
    "version": "0.2.0",
    "configurations": [
        {
            "name": "Pytest FlavaForPretrianing",
            "type": "python",
            "request": "launch",
            "module": "pytest",
            "args": ["${workspaceFolder}/tests/models/flava/test_modeling_flava.py::FlavaForPreTrainingIntegrationTest"],
            "env": {
                "RUN_SLOW": "1"
            },
            "justMyCode": true
        }
    ]
}
```
