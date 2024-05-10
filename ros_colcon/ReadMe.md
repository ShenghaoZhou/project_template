At the root of ros pixi workspace (pixi.toml location with ros installed), add the following task:  

ros_build="echo \"Build Project: $WS_DIR\" colcon build --build-base $WS_DIR --install-base $WS_DIR --event-handlers=console_direct+ --symlink-install --cmake-args -DCMAKE_EXPORT_COMPILE_COMMANDS=1 -DCMAKE_COLOR_DIAGNOSTICS=1 -GNinja"
