# Created by: Timothy Beyer <beyert@cs.ucr.edu>
# $FreeBSD$

PORTNAME=	gemrb
PORTVERSION=	0.8.0.1
PORTREVISION=	3
CATEGORIES=	games emulators
MASTER_SITES=	SF/${PORTNAME}/GemRB%20Sources/GemRB%20${PORTVERSION:.1=}%20Sources

MAINTAINER=	beyert@cs.ucr.edu
COMMENT=	GemRB (Game engine made with preRendered Background)

LICENSE=	GPLv2
LICENSE_FILE=	${WRKSRC}/COPYING

LIB_DEPENDS=	libpng.so:${PORTSDIR}/graphics/png \
		libvorbis.so:${PORTSDIR}/audio/libvorbis

OPTIONS_DEFINE=	DOCS

USES=		cmake openal:al,alut python shebangfix
SHEBANG_FILES=	admin/extend2da.py
USE_SDL=	sdl mixer ttf
USE_LDCONFIG=	yes
CFLAGS+=	-L${LOCALBASE}/lib -I${LOCALBASE}/include
CMAKE_C_FLAGS=	${CFLAGS}
CMAKE_ARGS=	-DDOC_DIR="${DOCSDIR}" -DMAN_DIR="${MAN6PREFIX}/man/man6/" -DDISABLE_WERROR=1 -DINSOURCEBUILD=1

.include <bsd.port.mk>
