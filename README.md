# Huffman

A Huffman coding implementation in Java. University project from 2021.

It reads a UTF-8 text file, counts character frequencies, builds the optimal prefix tree using a hand-written binary min-heap, encodes the text into its bit string, then decodes the bit string back and prints the result. Each phase reports how long it took in milliseconds.

The frequency table covers characters up to code point 10500 instead of plain ASCII, so Greek, Cyrillic and similar alphabets work too.

## Usage

Requires Java 11 or newer. From the project root:

```
java -jar Huffman.jar
```

To compress your own text, edit `Resources/prova.txt`.

One platform note: the input path is hardcoded as `Resources\prova.txt` with a Windows separator. On macOS or Linux, change line 120 of `Classses/Huffman.java` to `Resources/prova.txt` before running from source.

## Structure

- `Classses/Huffman.java` — frequency table, tree construction, encode and decode
- `Classses/MinHeap.java` — binary min-heap used while building the tree
- `Classses/BinaryTreeNode.java` — tree nodes
- `Classses/Main.java` — entry point wiring everything together
- `Resources/prova.txt` — sample input

Yes, the folder really is named "Classses". It was 2021.
