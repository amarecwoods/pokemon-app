# pokemon-app
Pokemon App Documentation

Overview

The Pokemon App is a simple application built using the Tkinter library in Python. It allows users to retrieve information about a Pokemon by entering its name. The application fetches data from the PokeAPI using the `pokebase` library and displays relevant information in a user-friendly interface.

 Components

1. CustomMessageBox Class

   The `CustomMessageBox` class represents a custom dialog box that displays information along with an optional image. It inherits from `tk.Toplevel` and is used to show Pokemon details.

   - Attributes:
     - `parent`: The parent window for the dialog box.
     - `title`: The title of the dialog box.
     - `info_message`: The message to be displayed in the dialog.
     - `image`: The image (optional) to be displayed in the dialog.

   - Methods:
     - `__init__(self, parent, title, info_message, image)`: Initializes the dialog box.
  
2. get_pokemon_info Function

   The `get_pokemon_info` function retrieves information about a Pokemon by making an API call to the PokeAPI using the `pokebase` library.

   - Parameters:
     - `pokemon_name`: The name of the Pokemon to fetch information for.

   - Returns:
     - An instance of the `pokebase.interface.APIResource` class containing Pokemon information.
      
3. PokemonApp Class

   The `PokemonApp` class represents the main application window. It includes a simple interface with entry fields and buttons for user interaction.

   - Attributes:
     - `root`: The main Tkinter window.
     - `image`: A reference to the PhotoImage instance for displaying Pokemon images.
   
   - Methods:
     - `__init__(self, root)`: Initializes the main application window.
     - `on_submit(self)`: Handles the button click event, fetches Pokemon information, and displays it.
     - `get_image_from_url(self, url)`: Downloads an image from a URL and returns a PhotoImage instance.
     - `convert_decimeters_to_feet(self, decimeters)`: Converts height from decimeters to feet.
     - `convert_hectograms_to_pounds(self, hectograms)`: Converts weight from hectograms to pounds.
     - `get_evolution_info(self, pokemon_info)`: Retrieves and formats evolution information for a Pokemon.

Usage

1. Installation

   Make sure you have the required libraries installed:

   ```bash
   pip install pillow requests pokebase
   ```

2. Running the App**

   Execute the script:

   ```bash
   python your_script_name.py
   ```

3. Interaction**

   - Enter the name of a Pokemon in the entry field.
   - Click the "Submit" button to fetch and display information.

Dependencies

- **Tkinter:** The standard GUI toolkit for Python.
- **Pillow (PIL):** Python Imaging Library for handling images.
- **Requests:** HTTP library for making API requests.
- **pokebase:** Python library for accessing the PokeAPI.

Pokebase info

- PokeAPI:The application fetches Pokemon data from the PokeAPI (https://pokeapi.co/).
- pokebase: The library used to interact with the PokeAPI (https://github.com/PokeAPI/pokebase).
