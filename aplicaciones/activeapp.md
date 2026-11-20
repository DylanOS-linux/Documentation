# Plasmoid DylanOS Active App

ID `com.dylanos.activeapp`. Muestra el nombre de la ventana activa mediante `TaskManager.TasksModel` y toma el ancho disponible del panel; si no hay una ventana activa, muestra «DylanOS». Si una aplicación no publica un nombre, usa su nombre genérico, app id o título visible, pero nunca la identifica como DylanOS. Se usa en la barra superior del layout inicial.

El mismo plasmoide muestra seis controles para toda ventana activa: nueva ventana, minimizar, maximizar/restaurar, mantener encima, menú de acciones y cerrar. Todas ejecutan operaciones reales de `TaskManager.TasksModel`; las capacidades que KWin no ofrece quedan desactivadas. El menú global `org.kde.plasma.appmenu` permanece a su lado para Archivo/Editar/Ver en las aplicaciones que lo exportan. No es un selector/lista de tareas: el dock inferior proporciona las tareas (`com.dylanos.dock`).

QML: `contents/ui/main.qml`; metadata: `metadata.json`. Ver [índice de plasmoids](search.md), [guía del escritorio](../guia/guia-de-uso.md) y [`test_shell_contract.py`](https://github.com/dylanneymarmontalvo2014-lgtm/DylanOS/blob/development/scripts/tests/test_shell_contract.py).
