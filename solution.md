```zsh
# Clone the initial repository
git clone git@github.com:eerwitt/command-line-mystery.git
cd command-line-mystery

# Check the status to see if anything is already marked as new (shouldn't be)
git status

# Edit my solution file
subl solution.md

# Commit initial solution
git add solution.md
git commit -a

# Start reading the instructions
less instructions

# Check for clues in the mystery
cd mystery
grep CLUE ./crimescene

// returns 3 clues. Male 6', member of AAA, Delta_Skymiles, local library, museam of Bash History, Annabel

cat People
//returns a ton of people!

grep "Annabel" people
//Returns addresses of Hart Place and Buckingham Place, line 179

cd mystery
head -n 179 Buckingham_Place | tail -n 1
// see interview 699607

cd interview
cat interview 699607
// returns "L337" "9" and Blue Honda

cd Vehicles
//returns a lot

grep -A 5 "L337" vehicles
// used hint for this//
//returns Joe Gerumsky and Jeremy Bowers

cd membership
cat AAA Delta_Skylines Museum_of_Bash_History | grep "Jeremy Bowers"
// suspect is Jeremy BOwers!!!!


