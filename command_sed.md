
echo test > test.txt

linux, use sed replace test to tttt

sed -i "s/test/tttt/g" \`grep -rl test *.txt\`

mac

sed -i "" "s/test/tttt/g" \`grep -rl test *.txt\`
