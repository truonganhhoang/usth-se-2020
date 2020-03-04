# Software Project Proposal: Palace

## Synopsis

[**Palace**][10] (Pythonic Audio Library and Codecs Environment) aims to be
a intuitive Python 3D audio API by wrapping around [alure][0], which in turn
is a high-level library using [OpenAL][1].

## Team

We are three second-year bachelor students from [USTH][2], whose student IDs
and GitHub handles are listed in the table below.

| Student ID |      Member      | GitHub handle |
| :--------: | ---------------- | :-----------: |
|  BI9-119   | Ngô Ngọc Đức Huy |   @Huy-Ngo    |
|  BI9-167   | Ngô Xuân Minh    |   @9a24f0     |
|  BI9-184   | Nguyễn Gia Phong |   @McSinyx    |

## Background

### Importance

3D audio effect is a technology that gives the audience an incredible experience
by manipulating speakers or headphones to simulate three-dimensional aural
sense. This is used predominantly in cinema, and, to a lesser extent,
video games.

With the recent trend in VR, 3D audio effect becomes increasingly important. It
is therefore a great necessity that there be a library for rendering 3D sound
effect.

### Related works

There were several other attempts at building an API for 3D sound effect before.
For Python in particular, there are three that can be listed, but each of them
has some disadvantages:
- [PySonic][3]: Abandoned, [wrapping around proprietary library][4]
- [PyOpenAL][5]: Unintuitive/low-level, few codecs support
- [pyglet][6]: Limited functionality

### Conclusion

Realizing that, we propose to start this project to build an interface to assist
developers in rendering 3D sounds.

## Objectives

### Target users

Our target users are any developers who are in need of a free/libre and
open source API for their projects.

### Expected deliverable

We aims to make **palace** to extend **OpenAL** the same way [**ModernGL**][7]
does to **OpenGL**.

The list of planned features includes:
- 3D sound rendering
- Environmental audio effects: reverberation, atmospheric air absorption,
  sound occlusion, and obstruction
- Binaural ([HRTF][8]) rendering
- Out-of-the-box audio decoding of common audio codecs
- Modern Pythonic API with type annotation, `with` context manager, etc.
- Portability: supporting GNU/Linux, Windows, macOS (and maybe others)


## Resources

In this project, we use [Cython][9] to wrap around the C++ API **alure**
to create a performant Python API for 3D audio.

## Measurement

Here are milestones that we are planning on:
- Codebase completion
- Tests
- Documentation and examples
- Packaging
- User feedback evaluation

## Risks

There are some possible risks that can be obstacles to our success:
- Packaging: not being able to finish packaging on time
- Not being able to wrap around the whole **alure** library due to the
  incomplete support of **Cython** to C++11
- The result ending up being as unfriendly as the currently available ones

In order to address these risks, we will analyze intensively requirements and
manage the workload and resource accordingly.

[0]: https://github.com/kcat/alure
[1]: https://www.openal.org/
[2]: https://usth.edu.vn/en/
[3]: http://pysonic.sourceforge.net/
[4]: https://fmod.com/licensing
[5]: https://pypi.org/project/PyOpenAL/
[6]: http://pyglet.org/
[7]: https://github.com/moderngl/moderngl
[8]: https://en.wikipedia.org/wiki/Head-related_transfer_function
[9]: https://cython.org/
[10]: https://github.com/McSinyx/palace
