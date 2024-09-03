<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sumner Floor Loot</title>
    <style>
        canvas {
            background-color: black;
            display: block;
            margin: 0 auto;
        }
        body {
            text-align: center;
            color: white;
            font-family: Arial, sans-serif;
            background-color: #111;
        }
        #infoBox {
            color: white;
            background-color: #333;
            padding: 10px;
            border-radius: 5px;
            margin: 10px auto;
            width: 80%;
            position: relative;
            border: 2px solid white; /* Added white outline */
        }
        #rarityDisplay, #itemDisplay {
            margin: 0;
            padding: 0;
        }
        #infoBox {
            padding-top: 13px; /* Add space for the rarity and item display */
        }
        .Common { color: white; }
        .Uncommon { color: green; }
        .Rare { color: blue; }
        .Epic { color: purple; }
        .Legendary { color: orange; }
        .Mythic { color: red; }
        .Exotic { color: gold; }
    </style>
</head>
<body>
    <h1>Sumner Floor Loot</h1>
    <div id="infoBox">
        <p id="rarityDisplay">Rarity: None</p>
        <p id="itemDisplay">Item: None</p>
    </div>
    <canvas id="gameCanvas"></canvas>

    <script>
        const canvas = document.getElementById('gameCanvas');
        const ctx = canvas.getContext('2d');
        const rarityDisplay = document.getElementById('rarityDisplay');
        const itemDisplay = document.getElementById('itemDisplay');
        canvas.width = window.innerWidth * 0.8;
        canvas.height = window.innerHeight * 0.8;

        const orbs = [];
        const particles = [];
        const rarities = {
            "Common": [
                "Paper Clip", "Penny", "Eraser", "Bit of Plastic", "Piece of Tape",
                "Gum", "Wrapper", "String", "Moldy Chip", "Mechanical Pencil",
                "Damaged Block Eraser", "Rubber Band", "Sticky Note", "Used Marker",
                "Chewed Up Pencil", "Old Test", "Paper Towel", "Plastic Fork",
                "Broken Ruler", "Pencil Shavings", "Scotch Tape"
            ],
            "Uncommon": [
                "Notebook", "Pen", "Stapler", "Glass Shard", "Used Toothbrush",
                "Pencil", "Dime", "Rubber Band", "Calculator", "Folder", "Highlighter",
                "Binder Clip", "Loose Leaf Paper", "Index Cards", "Blue Pen",
                "Red Pen", "Mechanical Pencil Refill", "Student ID", "Sticky Notes",
                "Folder Divider", "Mini Whiteboard"
            ],
            "Rare": [
                "Ring", "Rubber Duck", "Watch", "Battery", "Glue", "Sock", "Tiger Buck",
                "Pen Ink Cartridge", "Tooth?", "USB Drive", "Flash Drive", "Calculator",
                "Mini Flashlight", "Gum Packet", "Sharpener", "Pocket Knife", "Deck of Cards",
                "Spare Key", "Colored Pencils", "Tissue Box", "Keychain"
            ],
            "Epic": [
                "Headphones", "Wallet", "Smartphone", "Dollar Bill ", "Puddle of Something That Looks Like Oil",
                "Vape", "DC Motor", "Bluetooth Speaker", "Camera", "Action Figure", "Lunchbox",
                "Portable Charger", "Old Book", "Art Supplies", "Wireless Mouse", "Flashlight",
                "Small Plant", "Custom Mug", "Mini Puzzle", "Headphones Case", "Travel Pillow"
            ],
            "Legendary": [
                "Laptop", "Tablet", "Ring", "Scissors", "Laptop Charger", "Airpods",
                "Crying 6th Grader", "OboeTTV Merch ", "Spoon", "Digital Camera", "External Hard Drive",
                "Smartwatch", "High-end Notebook", "Gaming Console", "Bluetooth Earbuds", "Premium Backpack",
                "Portable Gaming Device", "Fancy Pen", "Organizer", "Rare Collectible", "Vintage Item"
            ],
            "Mythic": [
                "Literal Diamond", "Rolex", "OboeTTV Merch ", "20 Bucks", "Handbag",
                "Declaration of Independence", "3D Printed Dragon", "Gold Ring", "Vintage Jewelry",
                "Rare Art Piece", "Signed Memorabilia", "Gold Coin", "Luxury Watch", "Rare Antique",
                "Custom Artwork", "Limited Edition Book", "Exclusive Figurine", "Rare Currency", "Old Map",
                "Genuine Fossil", "Signed Sports Equipment"
            ],
            "Exotic": [
                "Gold Bar", "Platinum Credit Card", "Ancient Artifact", "Mystic Gem", "Rare Collectible",
                "Vintage Watch", "Crystal Skull", "Unique Sculpture", "Rare Coin", "Ancient Book",
                "Limited Edition Item", "Historical Relic", "Fossilized Remains", "Exotic Plant",
                "Precious Stone", "Luxury Pen", "Custom-made Jewelry", "High-end Electronics",
                "Historical Document", "Rare Painting", "Ancient Jewelry"
            ]
        };

        const rarityRanges = {
            "Common": [50, 70],
            "Uncommon": [20, 40],
            "Rare": [10, 15],
            "Epic": [3, 5],
            "Legendary": [1, 2],
            "Mythic": [0, 0.8],
            "Exotic": [0, 1]  // Made more common
        };

        const gravity = 0.2;
        const friction = 0.85;

        class Orb {
            constructor(x, y, radius, color, rarity) {
                this.x = x;
                this.y = y;
                this.radius = radius;
                this.color = color;
                this.rarity = rarity;
                this.dx = (Math.random() - 0.5) * 2;
                this.dy = (Math.random() - 0.5) * 2;
            }

            draw() {
                // Draw orb with outline
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.radius, 0, Math.PI * 2, false);
                ctx.fillStyle = this.color;
                ctx.fill();
                ctx.lineWidth = 2;
                ctx.strokeStyle = 'grey'; // Outline color
                ctx.stroke();
                ctx.closePath();

                // Draw reflection
                ctx.save();
                ctx.globalAlpha = 0.3; // Light reflection opacity
                ctx.translate(this.x + this.radius / 4, this.y - this.radius / 4);
                ctx.rotate(45 * Math.PI / 180); // Rotate 45 degrees
                ctx.beginPath();
                ctx.ellipse(0, 0, this.radius / 3, this.radius / 6, 0, 0, Math.PI * 2);
                ctx.fillStyle = 'white';
                ctx.fill();
                ctx.restore();
            }

            update(orbs) {
                if (this.y + this.radius + this.dy > canvas.height) {
                    this.dy = -this.dy * friction;
                    this.y = canvas.height - this.radius;  // Correct position if touching ground
                } else {
                    this.dy += gravity;
                }

                if (this.x + this.radius + this.dx > canvas.width) {
                    this.dx = -this.dx * friction;
                    this.x = canvas.width - this.radius;  // Correct position if touching right wall
                } else if (this.x - this.radius + this.dx < 0) {
                    this.dx = -this.dx * friction;
                    this.x = this.radius;  // Correct position if touching left wall
                }

                this.x += this.dx;
                this.y += this.dy;

                // Collision detection with other orbs
                for (let i = 0; i < orbs.length; i++) {
                    if (this === orbs[i]) continue;
                    const dist = Math.hypot(this.x - orbs[i].x, this.y - orbs[i].y);
                    if (dist < this.radius + orbs[i].radius) {
                        resolveCollision(this, orbs[i]);
                        preventOverlap(this, orbs[i], dist);
                    }
                }

                this.draw();
            }

            isClicked(x, y) {
                const dist = Math.hypot(x - this.x, y - this.y);
                return dist < this.radius;
            }
        }

        class Particle {
            constructor(x, y, dx, dy, radius, color) {
                this.x = x;
                this.y = y;
                this.dx = dx;
                this.dy = dy;
                this.radius = radius;
                this.color = color;
                this.alpha = 1;
            }

            draw() {
                ctx.save();
                ctx.globalAlpha = this.alpha;
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.radius, 0, Math.PI * 2, false);
                ctx.fillStyle = this.color;
                ctx.fill();
                ctx.closePath();
                ctx.restore();
            }

            update() {
                this.x += this.dx;
                this.y += this.dy;
                this.alpha -= 0.02;  // Smooth fade out
                if (this.alpha < 0) this.alpha = 0;  // Prevent flash before disappearing
                this.draw();
            }
        }

        function getRarity() {
            const roll = Math.random() * 100;
            for (const [rarity, [min, max]] of Object.entries(rarityRanges)) {
                if (roll >= min && roll <= max) {
                    return rarity;
                }
            }
            return "Common";  // Fallback
        }

        function generateOrbs() {
            for (let i = 0; i < 10; i++) {
                const radius = Math.random() * 30 + 20;
                const x = Math.random() * (canvas.width - radius * 2) + radius;
                const y = Math.random() * (canvas.height - radius * 2) + radius;
                const rarity = getRarity();
                const color = {
                    "Common": '#d3d3d3',  // Light gray for Common
                    "Uncommon": 'green',
                    "Rare": 'blue',
                    "Epic": 'purple',
                    "Legendary": 'orange',
                    "Mythic": 'red',
                    "Exotic": 'gold'
                }[rarity];
                orbs.push(new Orb(x, y, radius, color, rarity));
            }
            saveState();
        }

        function createParticles(x, y, color) {
            for (let i = 0; i < 8; i++) {
                const dx = (Math.random() - 0.5) * 2;
                const dy = (Math.random() - 0.5) * 2;
                particles.push(new Particle(x, y, dx, dy, Math.random() * 5 + 2, color));
            }
        }

        function resolveCollision(orb1, orb2) {
            const xVelocityDiff = orb1.dx - orb2.dx;
            const yVelocityDiff = orb1.dy - orb2.dy;

            const xDist = orb2.x - orb1.x;
            const yDist = orb2.y - orb1.y;

            if (xVelocityDiff * xDist + yVelocityDiff * yDist >= 0) {
                const angle = -Math.atan2(orb2.y - orb1.y, orb2.x - orb1.x);
                const m1 = orb1.radius;
                const m2 = orb2.radius;

                const u1 = rotate(orb1.dx, orb1.dy, angle);
                const u2 = rotate(orb2.dx, orb2.dy, angle);

                const v1 = { x: u1.x * (m1 - m2) / (m1 + m2) + u2.x * 2 * m2 / (m1 + m2), y: u1.y };
                const v2 = { x: u2.x * (m2 - m1) / (m1 + m2) + u1.x * 2 * m1 / (m1 + m2), y: u2.y };

                const finalV1 = rotate(v1.x, v1.y, -angle);
                const finalV2 = rotate(v2.x, v2.y, -angle);

                orb1.dx = finalV1.x;
                orb1.dy = finalV1.y;
                orb2.dx = finalV2.x;
                orb2.dy = finalV2.y;
            }
        }

        function preventOverlap(orb1, orb2, dist) {
            const overlap = orb1.radius + orb2.radius - dist;
            const smallDisplacement = overlap / 2;
            const angle = Math.atan2(orb2.y - orb1.y, orb2.x - orb1.x);

            orb1.x -= Math.cos(angle) * smallDisplacement;
            orb1.y -= Math.sin(angle) * smallDisplacement;
            orb2.x += Math.cos(angle) * smallDisplacement;
            orb2.y += Math.sin(angle) * smallDisplacement;
        }

        function rotate(dx, dy, angle) {
            return {
                x: dx * Math.cos(angle) - dy * Math.sin(angle),
                y: dx * Math.sin(angle) + dy * Math.cos(angle)
            };
        }

        function animate() {
            requestAnimationFrame(animate);
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            orbs.forEach((orb) => orb.update(orbs));
            particles.forEach((particle, index) => {
                particle.update();
                if (particle.alpha <= 0) {
                    particles.splice(index, 1);
                }
            });
        }

        canvas.addEventListener('click', (event) => {
            const rect = canvas.getBoundingClientRect();
            const mouseX = event.clientX - rect.left;
            const mouseY = event.clientY - rect.top;

            orbs.forEach((orb, index) => {
                if (orb.isClicked(mouseX, mouseY)) {
                    const rarity = orb.rarity;
                    const items = rarities[rarity];
                    const item = items[Math.floor(Math.random() * items.length)];
                    rarityDisplay.textContent = `Rarity: ${rarity}`;
                    itemDisplay.textContent = `Item: ${item}`;
                    rarityDisplay.className = rarity;  // Set class for color
                    itemDisplay.className = rarity;    // Set class for color
                    createParticles(orb.x, orb.y, orb.color);
                    orbs.splice(index, 1);  // Remove orb from array
                    saveState();
                }
            });

            if (orbs.length === 0) {
                generateOrbs();
            }
        });

        function saveState() {
            const savedOrbs = orbs.map(orb => ({
                x: orb.x,
                y: orb.y,
                radius: orb.radius,
                color: orb.color,
                rarity: orb.rarity
            }));
            localStorage.setItem('orbs', JSON.stringify(savedOrbs));
        }

        function loadState() {
            const savedOrbs = JSON.parse(localStorage.getItem('orbs'));
            if (savedOrbs) {
                savedOrbs.forEach(orbData => {
                    orbs.push(new Orb(
                        orbData.x,
                        orbData.y,
                        orbData.radius,
                        orbData.color,
                        orbData.rarity
                    ));
                });
            } else {
                generateOrbs();
            }
        }

        // Initialize game state
        loadState();
        animate();
    </script>
</body>
</html>
