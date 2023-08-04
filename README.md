# dev-env-customization
This repo contains files for customizing the Windows Terminal (Powershell, WSL) and VS Code Integrated Terminal using the [Starship](https://starship.rs/guide/) prompt engine and [Nerd Fonts](https://www.nerdfonts.com/). It also contains custom color scheme for Windows Terminal to go with the custom prompt.

# Setup
The Starship prompt is Cross-Shell you can use the Starship custom prompt file just about anywhere. However, this guide is geared towards Windows Terminals using PowerShell Core and WSL Ubuntu Bash.

1. Install a [Nerd Font](https://www.nerdfonts.com/)
    - Nerd Fonts provide the nifty icons which allow you to create custom prompts beyond the basic ASCII.
    - The choice is up to you but the one used in the preview pictures is 'IosevkaTerm Nerd Font'.
    - * Mono fonts may cause the icons to become very small

2. Install [Starship](https://starship.rs/guide/#step-1-install-starship)
    - Starship is the prompt engine that is used to build and customize the prompt. It is written in rust and is cross-shell meaning it will work just about anywhere.
    - If you are using WSL then this also needs to be done within the distribution if you want the custom prompt to apply there.

3. Configure your shell to use [Starship](https://starship.rs/guide/#step-2-set-up-your-shell-to-use-starship)
    - For powershell there are several [Profile](https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_profiles?view=powershell-7.3) options available that apply the customization in different scopes. To have the prompt apply more universally for your user, update the 'Current User, All Hosts' profile
    - If you are using WSL then this also needs to be done within the distribution if you want the custom prompt to apply there.

4. Get a local copy of the customization files
    - You can either clone this repository or download a copy locally

5. Configure [Starship](https://starship.rs/config/#prompt) to use custom prompt
    - Make a copy of the Starship TOML file that corresponds to the custom prompt you want and place it in your users .config folder with the name 'starship.toml' (yes, rename it). This method allows you to use the starship file as a starting point for your own customizations with out being tied to the changes made in the repository.
    - Alternatively you can point Starship to the specific prompt file you wish to impliment using environment variables. If you cloned the repository this is a good method to keep the file up to date with any changes made in the repository.
    - If you are using WSL then this also needs to be done within the distribution if you want the custom prompt to apply there.

6. Configure [Windows Terminal](https://learn.microsoft.com/en-us/windows/terminal/tutorials/custom-prompt-setup#install-a-nerd-font) to use Nerd Font
    - Just focus on the Nerd Font section as the rest of the guid goes into using Oh My Posh prompt engine.
    - Windows Terminal > Settings > {defaults | specific profile} > Appearence > Font Face > {Nerd Font you installed}

7. Configure [VS Code Integrated Terminal](https://code.visualstudio.com/docs/terminal/appearance#_text-style) to use Nerd Font
    - File > Preferences > Settings > Search Settings 'terminal integrated font family' > Add name of installed Nerd Font