```python
import tkinter as tk

def convert_to_upper(*args):
    # Get current input and convert to uppercase
    value = alphabet_var.get()
    alphabet_var.set(value.upper())

root = tk.Tk()
root.geometry("400x400")
root.title("Alphabet Converter")

alphabet_label = tk.Label(root, text="Enter any alphabet:")
alphabet_label.pack()

# Create StringVar to track changes
alphabet_var = tk.StringVar()
alphabet_var.trace_add("write", convert_to_upper)

alphabet_entry = tk.Entry(root, textvariable=alphabet_var)
alphabet_entry.pack()

root.mainloop()
```
