<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>🛠️ Pixel Art Generator (Theme Switch + Auto-Union)</title>
    <style>
        /* ======================== THEMES ======================== */
        /* --- LIGHT THEME (Default) --- */
        :root {
            --bg-color: #f6f8fa; /* Main background */
            --container-bg: #ffffff; /* Container background */
            --border-color: #e1e4e8;
            --text-color: #24292e;
            --header-bg: #f6f8fa;
            --heading-color: #586069;
            --input-bg: #f3f4f6;
            --code-bg: #f6f8fa;
            --note-color: #6a737d;
        }

        /* --- DARK THEME --- */
        body.dark-theme {
            --bg-color: #24292e;
            --container-bg: #1c2128;
            --border-color: #3e444b;
            --text-color: #c9d1d9;
            --header-bg: #1c2128;
            --heading-color: #8b949e;
            --input-bg: #2d333b;
            --code-bg: #2d333b;
            --note-color: #8b949e;
        }

        /* ======================== BASE STYLES ======================== */
        body { 
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen, Ubuntu, Cantarell, "Fira Sans", "Droid Sans", "Helvetica Neue", sans-serif; 
            background: var(--bg-color); 
            color: var(--text-color); 
            padding: 30px; 
            transition: background-color 0.3s, color 0.3s;
        }
        .container { 
            max-width: 900px; margin: 0 auto; 
            background: var(--container-bg); 
            border: 1px solid var(--border-color); 
            border-radius: 6px; 
            box-shadow: 0 3px 10px rgba(27,31,35,0.08); 
            transition: background-color 0.3s, border-color 0.3s;
        }
        
        .header { 
            padding: 16px; border-bottom: 1px solid var(--border-color); 
            background-color: var(--header-bg); 
            display: flex; justify-content: space-between; align-items: center;
        }
        h2 { font-size: 1.5em; color: var(--text-color); margin: 0; display: flex; align-items: center; }
        
        .content { padding: 24px; }
        .section-heading { 
            font-size: 1.2em; border-bottom: 1px solid var(--border-color); 
            padding-bottom: 5px; margin-top: 20px; margin-bottom: 15px; 
            color: var(--heading-color); font-weight: 600; 
        }
        
        /* Controls */
        .control-group { margin-bottom: 15px; display: flex; align-items: center; gap: 20px; }
        label { font-weight: 600; margin-right: 5px; }
        
        input[type="file"] { 
            margin-bottom: 10px; padding: 6px 12px; 
            border: 1px solid var(--border-color); border-radius: 6px; 
            background: var(--input-bg); color: var(--text-color);
            cursor: pointer; 
        }
        
        /* Slider */
        #pixelSizeSlider { width: 150px; height: 8px; background: var(--heading-color); border-radius: 4px; -webkit-appearance: none; appearance: none; margin: 0 10px; }
        #pixelSizeSlider::-webkit-slider-thumb { -webkit-appearance: none; appearance: none; width: 14px; height: 14px; border-radius: 50%; background: #28a745; cursor: pointer; border: 1px solid var(--container-bg); }
        #pixelSizeValue { font-weight: bold; color: #0366d6; width: 40px; text-align: right; }

        /* Buttons */
        .actions { margin-top: 20px; display: flex; gap: 10px; }
        button { 
            padding: 8px 16px; border-radius: 6px; cursor: pointer; font-weight: 600; 
            transition: background-color 0.1s, border-color 0.1s; border: 1px solid; 
        }
        
        #generateBtn { background-color: #2c974b; color: #fff; border-color: #2c974b; }
        #generateBtn:hover { background-color: #238636; }
        
        #resetBtn { background-color: #d73a49; color: #fff; border-color: #d73a49; }
        #resetBtn:hover { background-color: #c93340; }
        
        #copyBtn { 
            background-color: var(--container-bg); color: var(--text-color); border-color: var(--border-color); 
        }
        #copyBtn:hover { background-color: var(--input-bg); }

        /* Output & Preview */
        canvas { 
            border: 1px solid var(--border-color); image-rendering: pixelated; max-width: 100%; 
            margin-top: 15px; display: none; background: var(--container-bg); border-radius: 4px; 
        }
        
        textarea { 
            width: 100%; height: 300px; 
            background: var(--code-bg); color: var(--text-color); 
            border: 1px solid var(--border-color); 
            font-family: SFMono-Regular, Consolas, "Liberation Mono", Menlo, Courier, monospace; 
            padding: 10px; border-radius: 6px; resize: vertical; margin-top: 10px; 
            transition: background-color 0.3s, color 0.3s, border-color 0.3s;
        }
        
        #info { color: var(--heading-color); margin-top: 10px; font-size: 0.9em; }
        .note { font-size: 0.9em; color: var(--note-color); margin-top: 5px; }
    </style>
</head>
<body class="light-theme">

<div class="container">
    <div class="header">
        <h2>🛠️ Pixel Art Generator</h2>
        <button id="themeToggle" onclick="toggleTheme()" style="background-color: transparent; border: 1px solid var(--border-color); color: var(--text-color);">
            🌙 Theme
        </button>
    </div>
    
    <div class="content">
        <p>The generator optimizes pixels and creates code for the **Roblox Studio Command Bar**.</p>

        <div class="section-heading">1. Upload and Settings</div>

        <div class="control-group">
            <label>Select Image:</label>
            <input type="file" id="upload" accept="image/*">
        </div>

        <div class="control-group">
            <label for="pixelSizeSlider">Pixel Size (Studs):</label>
            <input type="range" id="pixelSizeSlider" min="0.1" max="5" step="0.1" value="1">
            <span id="pixelSizeValue">1.0</span> studs
        </div>
        
        <canvas id="preview"></canvas>
        <p id="info"></p>
        
        <div class="section-heading">2. Code Generation (Union Enabled)</div>

        <div class="actions">
            <button id="generateBtn" onclick="generateOptimizedCode()">Generate Code</button>
            <button id="resetBtn" onclick="resetApp()">Reset</button>
        </div>

        <p class="note">The code must be pasted into the **Command Bar** (View -> Command Bar) in Studio. Union will be performed automatically.</p>

        <textarea id="output" readonly placeholder="Generated Lua code will appear here..."></textarea>
        
        <div class="actions">
            <button id="copyBtn" onclick="copyToClipboard()">Copy Code</button>
        </div>
    </div>
</div>

<script>
    const fileInput = document.getElementById('upload');
    const canvas = document.getElementById('preview');
    const ctx = canvas.getContext('2d', { willReadFrequently: true });
    const output = document.getElementById('output');
    const info = document.getElementById('info');
    const slider = document.getElementById('pixelSizeSlider');
    const sliderValueDisplay = document.getElementById('pixelSizeValue');
    const themeToggle = document.getElementById('themeToggle');
    
    // Fixed constants
    let isLoaded = false;
    let originalWidth = 0;
    let originalHeight = 0;
    const THICKNESS = 0.2; 
    const TRANSPARENCY = 0; 
    const PAUSE_INTERVAL = 500; 
    const MAX_CHUNK_SIZE = 200; 
    const ENABLE_UNION = true; 

    // ======================== Theme Management ========================
    function toggleTheme() {
        const body = document.body;
        if (body.classList.contains('light-theme')) {
            body.classList.remove('light-theme');
            body.classList.add('dark-theme');
            themeToggle.innerHTML = '☀️ Theme';
        } else {
            body.classList.remove('dark-theme');
            body.classList.add('light-theme');
            themeToggle.innerHTML = '🌙 Theme';
        }
        updateCopyButtonColor(); 
    }

    function updateCopyButtonColor() {
        const isDark = document.body.classList.contains('dark-theme');
        const copyBtn = document.getElementById('copyBtn');
        if (isDark) {
            copyBtn.style.backgroundColor = '#1c2128'; 
            copyBtn.style.color = '#c9d1d9';
            copyBtn.style.borderColor = '#3e444b';
        } else {
            copyBtn.style.backgroundColor = 'var(--container-bg)'; 
            copyBtn.style.color = 'var(--text-color)';
            copyBtn.style.borderColor = 'var(--border-color)';
        }
    }
    document.addEventListener('DOMContentLoaded', updateCopyButtonColor);


    // ======================== Application Logic ========================
    slider.addEventListener('input', function() {
        sliderValueDisplay.textContent = parseFloat(this.value).toFixed(1);
    });

    fileInput.addEventListener('change', function(e) {
        const file = e.target.files[0];
        if (!file) return;
        const img = new Image();
        img.onload = function() {
            originalWidth = img.width;
            originalHeight = img.height;
            canvas.width = img.width;
            canvas.height = img.height;
            canvas.style.display = 'block';
            ctx.drawImage(img, 0, 0);
            info.innerText = `Size: ${originalWidth}x${originalHeight}. Image loaded.`;
            isLoaded = true;
        };
        img.src = URL.createObjectURL(file);
    });

    function resetApp() {
        fileInput.value = '';
        canvas.style.display = 'none';
        output.value = '';
        info.innerText = '';
        isLoaded = false;
        originalWidth = 0;
        originalHeight = 0;
        slider.value = 1;
        sliderValueDisplay.textContent = '1.0';
        alert("Reset complete.");
    }

    function generateOptimizedCode() {
        if (!isLoaded) { alert("Please upload an image first!"); return; }
        output.value = "Generating and optimizing... Please wait...";
        
        setTimeout(() => {
            const w = originalWidth;
            const h = originalHeight;
            const pSize = parseFloat(slider.value);

            if (isNaN(pSize) || pSize <= 0) {
                alert("Invalid pixel size.");
                output.value = "";
                return;
            }

            const imgData = ctx.getImageData(0, 0, w, h).data;
            let visited = new Array(h).fill(0).map(() => new Array(w).fill(false));
            let partsData = []; 

            function getColor(x, y) {
                if (x < 0 || x >= w || y < 0 || y >= h) return null;
                const idx = (y * w + x) * 4;
                if (imgData[idx + 3] === 0) return null; 
                return { r: imgData[idx], g: imgData[idx + 1], b: imgData[idx + 2] };
            }

            function colorsMatch(c1, c2) {
                return c1 && c2 && c1.r === c2.r && c1.g === c2.g && c1.b === c2.b;
            }

            // === GREEDY OPTIMIZATION ALGORITHM (finding rectangles) ===
            for (let y = 0; y < h; y++) {
                for (let x = 0; x < w; x++) {
                    const startColor = getColor(x, y);
                    if (visited[y][x] || !startColor) { 
                        if (!startColor) visited[y][x] = true; 
                        continue; 
                    }

                    let endX = x;
                    while (endX + 1 < w && !visited[y][endX + 1] && colorsMatch(startColor, getColor(endX + 1, y))) { endX++; }

                    let endY = y;
                    while (endY + 1 < h) {
                        let rowMatch = true;
                        for (let ix = x; ix <= endX; ix++) {
                            if (visited[endY + 1][ix] || !colorsMatch(startColor, getColor(ix, endY + 1))) {
                                rowMatch = false; break;
                            }
                        }
                        if (rowMatch) endY++; else break;
                    }

                    for (let iy = y; iy <= endY; iy++) {
                        for (let ix = x; ix <= endX; ix++) {
                            visited[iy][ix] = true;
                        }
                    }

                    partsData.push({
                        x: x, y: y,
                        width: endX - x + 1,
                        height: endY - y + 1,
                        color: startColor
                    });
                }
            }

            // === LUA CODE GENERATION ===
            
            let lua = `-- Optimized Generator for ${w}x${h} image.\n`;
            lua += `-- Total parts: ${partsData.length}. Compression: ${((w*h - partsData.length) / (w*h) * 100).toFixed(2)}%\n`;
            lua += `-- Configuration: Pixel Size: ${pSize} studs. Union: Enabled (Reliable Segmented)\n\n`;
            
            lua += `local GeometryService = game:GetService("GeometryService")\n`;
            lua += `local tempFolder = Instance.new("Folder", workspace) tempFolder.Name = "TempOptimizedPixelParts"\n`;
            lua += `local partsToUnion = {}\n`;
            lua += `local partCount = ${partsData.length}\n`;
            lua += `local PAUSE_INTERVAL = ${PAUSE_INTERVAL}\n`;
            lua += `local THICKNESS = ${THICKNESS};\n`;
            lua += `local TRANSPARENCY = ${TRANSPARENCY};\n\n`; 

            // 1. Create PartData table in Lua (to handle cross-language issues)
            lua += `local PartData = {\n`;
            partsData.forEach(pData => {
                const sizeX = (pData.width * pSize).toFixed(3);
                const sizeY = (pData.height * pSize).toFixed(3);
                // Calculate center position for the wall (XY plane)
                const centerX = ((pData.x * pSize) + ((pData.width * pSize) / 2)).toFixed(3);
                const centerY = (((h - pData.y) * pSize) - ((pData.height * pSize) / 2)).toFixed(3);
                
                const partSize = `{${sizeX}, ${sizeY}, THICKNESS}`;
                const partPos = `{${centerX}, ${centerY}, 0}`;

                lua += `    { Size = ${partSize}, Pos = ${partPos}, Color = {${pData.color.r}, ${pData.color.g}, ${pData.color.b}} },\n`;
            });
            lua += `}\n\n`;

            // 2. Part Creation Loop
            lua += `print(string.format("Starting creation of %d optimized blocks...", partCount))\n`;
            lua += `for i, data in ipairs(PartData) do\n`;
            lua += `    local p = Instance.new("Part")\n`;
            lua += `    p.Size = Vector3.new(data.Size[1], data.Size[2], data.Size[3])\n`;
            lua += `    p.Position = Vector3.new(data.Pos[1], data.Pos[2], data.Pos[3])\n`;
            lua += `    p.Color = Color3.fromRGB(data.Color[1], data.Color[2], data.Color[3])\n`;
            lua += `    p.Transparency = TRANSPARENCY\n`;
            lua += `    p.Anchored = true; p.CanCollide = false\n`;
            lua += `    p.Material = Enum.Material.SmoothPlastic\n`;
            lua += `    p.TopSurface = Enum.SurfaceType.Smooth; p.BottomSurface = Enum.SurfaceType.Smooth\n`;
            lua += `    p.Parent = tempFolder\n`;
            lua += `    table.insert(partsToUnion, p)\n`;
            lua += `    if i % PAUSE_INTERVAL == 0 then\n`;
            lua += `        print(string.format("Created %d/%d...", i, partCount)); task.wait()\n`;
            lua += `    end\n`;
            lua += `end\n\n`;
            
            // 3. AUTOMATIC RELIABLE SEGMENTED UNION LOGIC
            lua += `-- 3. RELIABLE SEGMENTED UNION LOGIC\n`;
            lua += `print("All blocks created. Starting segmented Union operation...")\n`;
            lua += `local MAX_CHUNK_SIZE = ${MAX_CHUNK_SIZE}\n`;
            lua += `local finalUnions = {}\n\n`;

            lua += `local function performUnion(partList)\n`;
            lua += `    local success, result = pcall(function() return GeometryService:UnionAsync(partList) end)\n`;
            lua += `    if success and result then\n`;
            lua += `        result.Anchored = true\n`;
            lua += `        result.Material = Enum.Material.SmoothPlastic\n`;
            lua += `        if partList[1] then result.Color = partList[1].Color end\n`;
            lua += `        return result\n`;
            lua += `    else\n`;
            lua += `        warn("Union set failed: " .. tostring(result) .. ". Leaving individual Parts.")\n`;
            lua += `        return nil\n`;
            lua += `    end\n`;
            lua += `end\n\n`;

            lua += `local currentChunk = {}\n`;
            lua += `for i, part in ipairs(partsToUnion) do\n`;
            lua += `    table.insert(currentChunk, part)\n`;
            lua += `    if #currentChunk >= MAX_CHUNK_SIZE or i == #partsToUnion then\n`;
            lua += `        print(string.format("--> Unionizing segment %d out of %d parts...", #finalUnions + 1, #currentChunk)); task.wait(0.1)\n`;
            lua += `        local unionPiece = performUnion(currentChunk)\n`;
            lua += `        if unionPiece then\n`;
            lua += `            unionPiece.Name = "PixelArtChunk_" .. #finalUnions + 1\n`;
            lua += `            table.insert(finalUnions, unionPiece)\n`;
            lua += `        end\n`;
            lua += `        currentChunk = {}\n`;
            lua += `    end\n`;
            lua += `end\n\n`;

            lua += `if #finalUnions == 0 then\n`;
            lua += `    warn("Final Union failed. Leaving individual Parts in TempOptimizedPixelParts.")\n`;
            lua += `    tempFolder.Parent = workspace\n`;
            lua += `    tempFolder.Name = "PixelArtParts_Failed"\n`;
            lua += `    return\n`;
            lua += `end\n\n`;

            lua += `print(string.format("Successfully created %d Union chunks. Attempting final Union...", #finalUnions))\n`;

            lua += `local finalResult = nil\n`;
            lua += `if #finalUnions == 1 then\n`;
            lua += `    finalResult = finalUnions[1]\n`;
            lua += `else\n`;
            lua += `    local success, result = pcall(function() return GeometryService:UnionAsync(finalUnions) end)\n`;
            lua += `    if success and result then\n`;
            lua += `        finalResult = result\n`;
            lua += `        print("Final Union successful.")\n`;
            lua += `    else\n`;
            lua += `        warn("Final Union failed. Leaving Union chunks.")\n`;
            lua += `        for _, u in ipairs(finalUnions) do u.Parent = workspace end\n`;
            lua += `        tempFolder:Destroy()\n`;
            lua += `        return\n`;
            lua += `    end\n`;
            lua += `end\n\n`;

            lua += `if finalResult then\n`;
            lua += `    finalResult.Name = "OptimizedPixelArt_FinalUnion"\n`;
            lua += `    finalResult.Parent = workspace\n`;
            lua += `    tempFolder:Destroy()\n`;
            lua += `    print("Done! Optimized art placed in Workspace.")\n`;
            lua += `end\n`;


            output.value = lua;
            info.innerText = `✅ Done! Created ${partsData.length} optimized blocks (Compression: ${((w*h - partsData.length) / (w*h) * 100).toFixed(2)}%).`;
        }, 50);
    }

    function copyToClipboard() {
        output.select();
        document.execCommand('copy');
        alert("Code copied to clipboard!");
    }
</script>

</body>
</html>
