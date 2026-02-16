// Exemplo de lógica de projeção ultra-compacta
// (x, y, z) são as coordenadas do ponto no mundo
let scale = fov / z; 
let screenX = x * scale + canvas.width / 2;
let screenY = y * scale + canvas.height / 2;

// Em vez de um modelo 3D, desenhamos o ponto
ctx.fillStyle = `rgba(255,255,255,${1/z})`; // O ponto some no escuro (z)
ctx.fillText(".", screenX, screenY);
