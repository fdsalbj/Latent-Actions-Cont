# Latent-Actions-Cont
Contains example projects for the feature contained in [this pull request](https://github.com/EpicGames/UnrealEngine/pull/1752)

TestLatent Scene - The level blueprint demonstrates calling several latent actions from functions
  
TestCont Scene - Shows how to use Continuations to turn MediaPlayer::OpenURL into a latent action using only blueprints. Note that OpenURL is still synchronous in 4.10, but is now async in the Master branch. For this reason the async OnMediaOpened event is simulated here with Delay. Other MediaPlayer operations such as Play, Pause, Seek, SetRate can't be applied until the media is successfully opened. This makes it a pita to use them with events, but it becomes a trivial matter thanks to the latent action.

TestCoroutine Scene - Shows an example of Lua-like coroutines

TestFork Scene - Shows an example of running latent actions in parallel with Fork and Join nodes

A bit of [documentation](http://unktomi.github.io/Latent-Actions-Cont/Cont.html)
