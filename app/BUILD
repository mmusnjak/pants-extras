python_sources()

pex_binary(
    name="app_binary",
    execution_mode="venv",
    dependencies=[
        ":app",
        "3rdparty/python:uvicorn",  # This isn't imported anywhere, so dependency inference doesn't find it.
    ],
    platforms=["linux_x86_64-cp-3.8-cp38m"],
    shebang="/usr/bin/env python3.8" # I would expect this to be set correctly from interpreter constraints
)

docker_image(
    name="app_image",
    source="Dockerfile",
)
