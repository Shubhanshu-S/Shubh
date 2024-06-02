// Create a variable to hold your NFTs
const NFTs = [];

// This function will take in some values as parameters, create an
// NFT object using the parameters passed to it for its metadata, 
// and store it in the variable above.
function mintNFT(_name, _city, _age, _cloth, _clothColor) {
    if (typeof _name !== 'string' || typeof _city !== 'string' || typeof _age !== 'number' || typeof _cloth !== 'string' || typeof _clothColor !== 'string') {
        console.log("Error: Invalid input types. Please check the inputs.");
        return;
    }
    const NFT = {
        name: _name,
        city: _city,
        age: _age,
        cloth: _cloth,
        clothColor: _clothColor,
    };
    NFTs.push(NFT);
    console.log("Minted: " + _name);
}

// Create a "loop" that will go through an "array" of NFTs
// and print their metadata with console.log()
function listNFTs() {
    if (NFTs.length === 0) {
        console.log("No NFTs minted yet.");
        return;
    }
    for (let i = 0; i < NFTs.length; i++) {
        console.log(`\nID:\t\t${i + 1}`);
        console.log(`Name:\t\t${NFTs[i].name}`);
        console.log(`City:\t\t${NFTs[i].city}`);
        console.log(`Age:\t\t${NFTs[i].age}`);
        console.log(`Cloth:\t\t${NFTs[i].cloth}`);
        console.log(`Cloth Color:\t${NFTs[i].clothColor}`);
    }
}

// Print the total number of NFTs we have minted to the console
function getTotalSupply() {
    console.log(`\nTotal NFTs Minted: ${NFTs.length}`);
}

// Call your functions below this line
mintNFT("Ram", "Chandigarh", 21, "Shirt", "Orange");
mintNFT("Shyam", "Delhi", 11, "T-Shirt", "Yellow");
mintNFT("Shiv", "Varanasi", 28, "Shirt", "White");

listNFTs();
getTotalSupply();
