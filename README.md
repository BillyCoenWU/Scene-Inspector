# Scene Inspector 🎮

![Unity](https://img.shields.io/badge/Unity-100000?style=flat-square&logo=unity&logoColor=white)
![C#](https://img.shields.io/badge/C%23-239120?style=flat-square&logo=c-sharp&logoColor=white)

[![Unity 2019.4+](https://img.shields.io/badge/unity-2019.4%2B-blue.svg)](https://unity3d.com/get-unity/download)
![GitHub last commit](https://img.shields.io/github/last-commit/RGSMS/Scene-Inspector)
![GitHub all releases](https://img.shields.io/github/downloads/RGSMS/Scene-Inspector/total)
![GitHub](https://img.shields.io/github/license/RGSMS/Scene-Inspector)

[![Roadmap](https://img.shields.io/badge/roadmap-blue.svg)](https://trello.com/b/O3IBSlWV)

[![Twitter Follow](https://img.shields.io/twitter/follow/rologsms?style=social)](https://twitter.com/rologsms)

## A custom serialization of a scene's informations in the unity inspector.

You will no longer insert the wrong scene name when typing it in the string field. In addition, you can decide to load a scene using the `Path`, `Name` or `Build Index` without worrying about changes that can be made to the selected scene.

_What this allows you to do:_

1. _Select scenes from any project folder and serialize the information in the Unity inspector;_
2. _Stores the `Path`, `Name` and `Build Index` informations from selected scene;_
3. _Keeps your selected scene's `Build Index` updated if you change the order of scenes in the build settings;_
4. _Keeps your selected scene's `Path` updated if you change the scene's folder_

## How to use:

Create a _`SceneInspector`_ variable:
```c#
[SerializeField]
private SceneInspector _scene = null;
```

Configure the scene in the inspetor:

![ ](https://github.com/RGSMS/prints/blob/main/printjpg.jpg)

Choose which scene info you will use to load the scene:
```c#
SceneManager.LoadSceneAsync(_scene.BuildIndex);
//or
SceneManager.LoadSceneAsync(_scene.Name);
//or
SceneManager.LoadSceneAsync(_scene.Path);
```
