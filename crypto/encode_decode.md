# Encode → Text to Base64
echo "test" | base64

# Encode → Hex to Bytes
echo "<HEX>" | xxd -r -p

# Decode → Base64 to Bytes
echo "<base64data>" | base64 -d

# Decode → Bytes to Hex
echo "<Bytes>" | xxd -p
