# :pencil: Neovim as an Code Editor for Unity

> :bulb: This repository aims to provide integration of Neovim as an external editor in Unity

This repo was previously archived due to a [maintained fork from TheArgus](https://github.com/the-argus/com.unity.ide.neovim.git), but unarchived in order to update the "Open External Editor" Unity logic and to add information

# :hammer_and_wrench: Installation

### Clone this repo
``git clone https://github.com/niscolas/com.unity.ide.neovim.git``

### Install the package
Open Unity. Go to Window > Package Manager and select the "+" sign at the top
left of the window. From the dropdown, select "Add package from disk". Browse
and select the ``package.json`` file at the root of this repo.

### Select Neovim as the editor
Go to Edit > Preferences > External Tools.
Set "External Script Editor" to "Neovim" in the dropdown menu. If it's not
present, then select "browse" and select the file ``run.sh`` at the root of
this repo.

### Customize run.sh
It's necessary to customize the ``run.sh`` file to fit your needs. Open it and
make sure the ``term_exec`` variable matches your own terminal emulator.

## :grey_exclamation: Notes / Precautions
Keep in mind that as of right now the integration between Omnisharp-roslyn LSP server has the following related issues: 
 - https://github.com/OmniSharp/omnisharp-roslyn/issues/2250#issuecomment-1363349360)
 - https://github.com/neovim/neovim/issues/14042
 - https://github.com/OmniSharp/omnisharp-roslyn/issues/2250
That means that despite allowing the user to use Neovim as an external editor for Unity and to reload the project files, this repository 
